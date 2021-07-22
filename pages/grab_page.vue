<template>
    <div class="bg-gradient-cartree">
        <div class="container mt-3">
            <div class="row">
                <div class="col-12 col-lg-1 pr-0 mr-4">
                    <img
                        class="rounded-circle"
                        src="/logo/grab.jpg"
                        width="70"
                        alt=""
                    />
                </div>
                <div
                    class="col-10 col-lg-10 ml-3 ml-lg-0 pl-0 d-flex align-items-center"
                >
                    <h1 class="text-bingsu-blue">Grab Holdings Inc.</h1>
                </div>
            </div>
            <div class="row mt-3">
                <div class="col-12 col-lg-6">
                    <div
                        class="card"
                        style="width: 100%; border-radius: 20px; background-color: rgba(0, 0, 0, 0.1);"
                    >
                        <div class="card-body">
                            <h3 class="text-white">Grab Summary</h3>
                            <div class="text-white mb-4">
                                Mon 2 - Sun 8 August 2021
                            </div>
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

            <ranking-card></ranking-card>

			<div class="row" style="height:30px">
			</div>
        </div>
    </div>
</template>
<script>
import "~/assets/css/app_page.css";
import "~/assets/css/index.css";

import RankingCard from "~/components/ranking_card.vue"
import DoughnutElem from "~/components/doughnut_elem.vue";


export default {
    layout: "main",
    components: {
        RankingCard,
		DoughnutElem
    },
    data() {
        return {
			dataDonut: {
                labels: ["Grab", "Others"],
                data: [250, 540],
                backgroundColor: ["rgba(68, 207, 95, 1)", "rgba(0, 0, 0, 0.1)"],
                unit: "kg of Carbon",
                text: "Carbon Emissions"
            },
            data: {
                labels: [
                    "Monday",
                    "Tuesday",
                    "Wednesday",
                    "Thursday",
                    "Friday",
                    "Saturday",
                    "Sunday"
                ],
                datasets: [
                    {
                        label: "kg of Carbon",
                        data: [180, 386, 298, 112, 438, 230, 379],
                        backgroundColor: "rgba(68, 207, 95, 1)",
                        borderWidth: 0,
                    }
                ]
            },
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
