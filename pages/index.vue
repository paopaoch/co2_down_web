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

			<footer-phone></footer-phone>
        </div>
    </div>
</template>
<script>
import Donut from "vue-css-donut-chart";
import "vue-css-donut-chart/dist/vcdonut.css";
import Vue from "vue";
import "~/assets/css/index.css";
import FooterPhone from "~/components/footer_phone.vue"

Vue.use(Donut);

export default {
	components: {
		FooterPhone
	},
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
