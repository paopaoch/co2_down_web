<template>
    <div>
        <div class="container-fluid bg-gradient">
            <div class="row">
                <div class="col-2 offset-2">
                    <vc-donut
                        background="#9fd4da"
                        :size="400"
                        unit="px"
                        :thickness="50"
                        :has-legend="false"
                        legend-placement="top"
                        :sections="sections"
                        :total="100"
                        :start-angle="10"
                        :auto-adjust-text-size="false"
                        @section-click="handleSectionClick"
                        @section-mouseover="handleSectionHover"
                        class="text-bingsu-blue"
                    >
                        <h5 class="text-donut"
                            >Total CO<sub>2</sub> Emission</h5>
                        <h2>7809 kg</h2>
                    </vc-donut>
                </div>
                <div
                    class=" col-8 d-flex justify-content-center align-items-center"
                >
                    <h3>something here kid yung mai ork</h3>
                </div>
            </div>

            <div class="row">
                <div class="col-8 text-center my-auto">
                    <h3>here na ja pen pic from the tree planting</h3>
                    <h3>but we dont have that yet lmao</h3>
                    <h3>we can make it up 5555</h3>
                    <h3>55555555</h3>
                </div>
                <div class="col-2">
                    <vc-donut
                        background="#a9d0e1"
                        :size="400"
                        unit="px"
                        :thickness="50"
                        :has-legend="false"
                        legend-placement="top"
                        :sections="sections2"
                        :total="100"
                        :start-angle="0"
                        :auto-adjust-text-size="false"
                        @section-click="handleSectionClick"
                        @section-mouseover="handleSectionHover"
                        class="text-bingsu-blue"
                    >
                        <h5 class="text-donut"
                            >Trees planted</h5
                        >
                        <h1>{{sections2[0].value}}%</h1>
                    </vc-donut>
                </div>
            </div>

			<div style="height: 25vh;"></div>

            <footer
                class="text-lg-start pt-5 mt-5"
                style="background-color: transparent;"
            >
                <!-- Grid container -->
                <div class="container">
                    <!--Grid row-->
                    <div class="row">
                        <!--Grid column-->
                        <div class="col-md-6 mb-4 mb-md-0">
                            <div class="row text-white">
                                <h1>
                                    Track Your Order’s Carbon Footprint Now!
                                </h1>
                                <p class="text-footer">
                                    CO2L Down helps you become more sustainable
                                    by tracking the Carbon Emission of your food
                                    delivery. Join the monthly leaderboard for
                                    prizes, coins, and discounts! You can also
                                    donate to our Tree Planting initiative to
                                    offset your carbon footprint. Simply link
                                    CO2L Down to your food delivery apps, and
                                    contribute to a better world today.
                                </p>
                                <div class="text-footer">
                                    [this but in Thai]
                                </div>
                            </div>
                            <div class="row">
                                <div class="col-6 mt-3 pl-0">
                                    <img
                                        src="/graphic-design.png"
                                        width="40"
                                        alt=""
                                    />
                                    <h6 class="mt-1">Simple to use</h6>
                                    <div class="text-footer text-muted">
                                        Automatically calculates Carbon Emission
                                        for you. No need for data logs.
                                    </div>
                                </div>
                                <div class="col-6 mt-3 p-0">
                                    <img
                                        src="/graphic-design.png"
                                        width="40"
                                        alt=""
                                    />
                                    <h6 class="mt-1">Donate</h6>
                                    <div class="text-footer text-muted">
                                        Helps us plant trees and offset your carbon footprint.
                                    </div>
                                </div>
                            </div>
                            <div class="row mb-4">
                                <div class="col-6 mt-3 pl-0">
                                    <img
                                        src="/graphic-design.png"
                                        width="40"
                                        alt=""
                                    />
                                    <h6 class="mt-1">Win monthly Leaderboards</h6>
                                    <div class="text-footer text-muted">
                                        Most efficient users get more Carbon
                                        Coins which can be exchanged for
                                        discounts. Complete milestones to earn
                                        more Coins.
                                    </div>
                                </div>
                                <div class="col-6 mt-3 p-0">
                                    <img
                                        src="/graphic-design.png"
                                        width="40"
                                        alt=""
                                    />
                                    <h6 class="mt-1">Redeem Rewards</h6>
                                    <div class="text-footer text-muted">
                                        Use Carbon Coins to redeem restaurant and delivery discounts.
                                    </div>
                                </div>
                            </div>
                        </div>
                        <!--Grid column-->

                        <!--Grid column-->
                        <div class="offset-md-1 col-md-5 mb-4 mb-md-0 div-wrapper">
                            <img src="/Picture6.png" width="450" alt="" />
                        </div>
                        <!--Grid column-->
                    </div>
                    <!--Grid row-->
                </div>
                <!-- Grid container -->
            </footer>
        </div>
    </div>
</template>
<script>
import Donut from "vue-css-donut-chart";
import "vue-css-donut-chart/dist/vcdonut.css";
import Vue from "vue";
import "~/assets/css/index.css";

Vue.use(Donut);

export default {
    layout: "main",
    data() {
        return {
            sections: [
                { label: "Grab section", value: 30, color: "#8755ec" },
                { label: "Food panda section", value: 30, color: "#f068c5" },
                { label: "Robin hood section", value: 40, color: "#44cf5f" }
            ],
			sections2: [
                { label: "Trees section", value: 32, color: "#56d794" }
            ]
        };
    },
    methods: {
        handleSectionClick(section, event) {
            console.log(`${section.label} clicked.`);
        },
        handleSectionHover(section, event) {
            console.log(`${section.label} hover.`);
        }
    }
};
</script>
