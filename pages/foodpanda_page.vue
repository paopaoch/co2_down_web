<template>
    <div class="bg-gradient-cartree">
        <div class="container mt-3">
            <div class="row">
                <div class="col-12 col-lg-1 pr-0 mr-4">
                    <img
                        class="rounded-circle"
                        src="/logo/food_panda.png"
                        width="70"
                        alt=""
                    />
                </div>
                <div
                    class="col-10 col-lg-10 ml-3 ml-lg-0 pl-0 d-flex align-items-center"
                >
                    <h1 class="text-bingsu-blue">Foodpanda</h1>
                </div>
            </div>
            <div class="row mt-3">
                <div class="col-12 col-lg-6">
                    <div
                        class="card"
                        style="width: 100%; border-radius: 20px; background-color: rgba(0, 0, 0, 0.1);"
                    >
                        <div class="card-body">
                            <h3 class="text-white">Foodpanda Summary</h3>
                            <date-for-card></date-for-card>
                            <bar-bingsu
                                :chartdata="data"
                                :options="options"
                            ></bar-bingsu>
                        </div>
                    </div>
                </div>
                <div class="col-12 col-lg-6 mt-4 mt-lg-0 postion-relative">
                    <doughnut-elem
                        class="postion-absolute"
                        style="z-index: 2; width: 100%; height: 100%;"
                        :labels="dataDonut.labels"
                        :data="dataDonut.data"
                        :backgroundColor="dataDonut.backgroundColor"
                        :unit="dataDonut.unit"
                        :text="dataDonut.text"
                    ></doughnut-elem>
                </div>
            </div>

            <ranking-card :ranks="ranks"></ranking-card>
            <div class="row" style="height:30px"></div>
        </div>
    </div>
</template>
<script>
import "~/assets/css/app_page.css";
import "~/assets/css/index.css";

import RankingCard from "~/components/ranking_card.vue";
import DoughnutElem from "~/components/doughnut_elem.vue";
import DateForCard from "~/components/date_for_card.vue"
import axios from "axios";

export default {
    async asyncData() {
        // API for trees
        const carbon = await axios.post(
            "https://isvonshaljavzm4qc3g3xmwepm.appsync-api.ap-southeast-1.amazonaws.com/graphql",
            {
                query: `query MyQuery {
							getTotalCarbonSum {
								status
								data {
								foodpanda
								grab
								robinhood
								}
							}
						}`
            },
            {
                headers: {
                    "x-api-key": process.env.API_KEY
                }
            }
        );
        const foodpanda = carbon.data.data.getTotalCarbonSum.data.foodpanda;
        const others =
            carbon.data.data.getTotalCarbonSum.data.grab +
            carbon.data.data.getTotalCarbonSum.data.robinhood;

        const top100Rank = await axios.post(
            "https://isvonshaljavzm4qc3g3xmwepm.appsync-api.ap-southeast-1.amazonaws.com/graphql",
            {
                query: `query MyQuery {
							getAllUserRanking(company: "foodpanda", top_100: true, user_id: "none") {
								data {
									username
									foodpanda_points
								}
								status
							}
						}`
            },
            {
                headers: {
                    "x-api-key": process.env.API_KEY
                }
            }
        );
        let rankList = top100Rank.data.data.getAllUserRanking.data.slice(0, 9);
        let ranks = [];
        for (let i = 0; i < rankList.length; i++) {
            ranks.push({
                name: rankList[i].username,
                points: rankList[i].foodpanda_points
            })
        };

		const dayBarData = await axios.post(
            "https://isvonshaljavzm4qc3g3xmwepm.appsync-api.ap-southeast-1.amazonaws.com/graphql",
            {
                query: `query MyQuery {
							getTotalCo2AmountByCompany {
								data {
									day
									foodpanda
								}
								status
							}
						}`
            },
            {
                headers: {
                    "x-api-key": process.env.API_KEY
                }
            }
        );
		let dayLabels = []
		let barData = []
		dayBarData.data.data.getTotalCo2AmountByCompany.data.slice().reverse().forEach(element => {
			dayLabels.push(element.day)
			barData.push(element.foodpanda.toFixed(4))
		});
        return {
			ranks,
            dataDonut: {
                labels: ["Foodpanda", "Others"],
                data: [foodpanda.toFixed(4), others.toFixed(4)],
                backgroundColor: ["rgba(215, 3, 101, 1)", "rgba(0, 0, 0, 0.1)"],
                unit: "g of Carbon",
                text: "Carbon Emissions"
            },
			data: {
                labels: dayLabels,
                datasets: [
                    {
                        label: "g of Carbon",
                        data: barData,
                        backgroundColor: "rgba(215, 3, 101, 1)",
                        borderWidth: 0
                    }
                ]
            },
        };
    },
    layout: "main",
    components: {
        DoughnutElem,
        RankingCard,
		DateForCard
    },
    data() {
        return {
            options: {
                maintainAspectRatio: false,
                scales: {
                    yAxes: [
                        {
                            label: {
                                display: false
                            },
                            ticks: {
                                beginAtZero: true,
                                fontColor: "white"
                            },
                            gridLines: {
                                display: false
                            }
                        }
                    ],
                    xAxes: [
                        {
                            barPercentage: 0.25,
                            ticks: {
                                beginAtZero: true,
                                fontColor: "white"
                            },
                            gridLines: {
                                display: false
                            }
                        }
                    ]
                },
                legend: {
                    display: false
                }
            }
        };
    }
};
</script>
