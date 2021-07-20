<template>
    <div class="bg-gradient-cartree">
        <div class="container mt-3">
            <div class="row">
                <div class="col-1 pr-0 mr-4">
                    <img
                        class="rounded-circle"
                        src="/logo/grab.jpg"
                        width="70"
                        alt=""
                    />
                </div>
                <div class="col-8 pl-0 d-flex align-items-center">
                    <h1 class="text-bingsu-blue">Grab Holdings Inc.</h1>
                </div>
            </div>
            <div class="row mt-3">
                <div class="col-6">
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
                <div class="col-6 m-auto">
                    <div>
                        <vc-donut
                            background="#c7e5e9"
                            :size="400"
                            unit="px"
                            :thickness="40"
                            :has-legend="false"
                            legend-placement="top"
                            :sections="sections"
                            :total="100"
                            :start-angle="0"
                            :auto-adjust-text-size="false"
                            class="text-bingsu-blue"
                        >
                            <h5 class="text-donut">CO<sub>2</sub> Emission</h5>
                            <h2 class="text-head-donut">35%</h2>
                        </vc-donut>
                    </div>
                </div>
            </div>

			
            <div
                class="card mt-4"
                style="width: 100%; border-radius: 20px; background-color: rgba(0, 0, 0, 0.1);"
            >
                <div class="card-body">
					<div class="row">
						<div class="col-4 d-flex justify-content-center">
							<h3 class="text-white">Top Players Last Week</h3>
						</div>
					</div>
                    <div class="row">
                        <div class="col-4 d-flex justify-content-center">
                            <b-list-group
                                class="text-white"
                                style="width: 300px;"
                            >
                                <ranking-elem
                                    rank="1"
                                    name="Sakupao"
                                    points="4202"
                                ></ranking-elem>
                                <ranking-elem
                                    rank="2"
                                    name="Grace_a"
                                    points="4110"
									variant="primary"
                                ></ranking-elem>
                                <ranking-elem
                                    rank="3"
                                    name="yumi-mosa"
                                    points="4105"
									variant="danger"
                                ></ranking-elem>
                            </b-list-group>
                        </div>
						<div class="col-4 d-flex justify-content-center">
                            <b-list-group
                                class="text-white"
                                style="width: 300px;"
                            >
                                <ranking-elem
                                    rank="4"
                                    name="DelG"
                                    points="4026"
									variant="warning"
                                ></ranking-elem>
                                <ranking-elem
                                    rank="5"
                                    name="MimImiM"
                                    points="3500"
									variant="success"
                                ></ranking-elem>
                                <ranking-elem
                                    rank="6"
                                    name="mosa-yumi"
                                    points="3456"
									variant="primary"
                                ></ranking-elem>
                            </b-list-group>
                        </div>
						<div class="col-4 d-flex justify-content-center">
                            <b-list-group
                                class="text-white"
                                style="width: 300px;"
                            >
                                <ranking-elem
                                    rank="7"
                                    name="Sakupao2"
                                    points="3234"
									variant="info"
                                ></ranking-elem>
                                <ranking-elem
                                    rank="8"
                                    name="ENae"
                                    points="3156"
                                ></ranking-elem>
                                <ranking-elem
                                    rank="9"
                                    name="GaiGinKo"
                                    points="3048"
									variant="warning"
                                ></ranking-elem>
                            </b-list-group>
                        </div>
                    </div>
                </div>
            </div>

			<div class="row" style="height:30px">
			</div>
        </div>
    </div>
</template>
<script>
import "~/assets/css/app_page.css";
import "~/assets/css/index.css";

import RankingElem from "~/components/ranking_elem.vue";

import Donut from "vue-css-donut-chart";
import "vue-css-donut-chart/dist/vcdonut.css";
import Vue from "vue";
Vue.use(Donut);

export default {
    layout: "main",
    components: {
        RankingElem
    },
    data() {
        return {
            sections: [{ label: "Grab", value: 35, color: "#44cf5f" }],
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
