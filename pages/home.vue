<template>
    <div>
        <div class="container-fluid bg-gradient">
            <div class="row">
                <div
                    class="col-md-5 text-bingsu-blue d-sm-block d-md-none text-center"
                >
                    <h3 class="text-donut">
                        Season:
                    </h3>
                    <h1 class="text-head-donut">July 2021</h1>
                    <h3 class="text-donut">Users:</h3>
                    <h1 class="text-head-donut">2,498</h1>
					<h3 class="text-donut">Total CO<sub>2</sub>:</h3>
                    <h1 class="text-head-donut">{{totalCO2}} kg</h1>
                    <h6>Look at weekly reports:</h6>
                    <div>
                        <NuxtLink to="/grab_page">
                            <img
                                class="application"
                                src="/logo/grab.jpg"
                                width="80"
                                alt=""
                            />
                        </NuxtLink>

                        <NuxtLink to="/foodpanda_page">
                            <img
                                class="m-2 application"
                                src="/logo/food_panda.png"
                                width="80"
                                alt=""
                            />
                        </NuxtLink>

                        <NuxtLink to="/robinhood_page">
                            <img
                                class="application"
                                src="/logo/Robinhood-APK-MOD-Download-1.8.0.png"
                                width="80"
                                alt=""
                            />
                        </NuxtLink>
                    </div>
                </div>
                <div class="col-12 col-md-7 mt-4 mt-md-0 postion-relative">
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
                <div
                    class="col-md-5 text-bingsu-blue d-none d-md-block"
                    style="height: 600px;"
                >
                    <h3 class="text-donut">
                        Season
                    </h3>
                    <h1 class="text-head-donut">July 2021</h1>
                    <h3 class="text-donut">Users:</h3>
                    <h1 class="text-head-donut">2,498</h1>
					<h3 class="text-donut">Total CO<sub>2</sub>:</h3>
                    <h1 class="text-head-donut">{{totalCO2}} kg</h1>
                    <h6>Look at weekly reports:</h6>
                    <div>
                        <NuxtLink to="/grab_page">
                            <img
                                class="application image"
                                src="/logo/grab.jpg"
                                width="80"
                                alt=""
                            />
                        </NuxtLink>

                        <NuxtLink to="/foodpanda_page">
                            <img
                                class="m-2 application image"
                                src="/logo/food_panda.png"
                                width="80"
                                alt=""
                            />
                        </NuxtLink>

                        <NuxtLink to="/robinhood_page">
                            <img
                                class="application image"
                                src="/logo/Robinhood-APK-MOD-Download-1.8.0.png"
                                width="80"
                                alt=""
                            />
                        </NuxtLink>
                    </div>
                </div>
            </div>

            <div class="row mt-4">
				<div class="col-12 my-auto text-bingsu-blue d-sm-block d-md-none text-center">
                    <h3 class="text-donut" style="padding-top: 100px">Trees Planted</h3>
                    <h1 class="text-head-donut">{{ trees }}</h1>
                    <h3 class="text-donut">Carbon Emission Offset*</h3>
                    <h1 class="text-head-donut">3000 kg</h1>
                    <h6>*When fully grown (in one year)</h6>
                </div>
                <div class="col-3 offset-2 my-auto text-bingsu-blue d-none d-md-block" style="height: 600px;">
                    <h3 class="text-donut" style="padding-top: 100px">Trees Planted</h3>
                    <h1 class="text-head-donut">{{ trees }}</h1>
                    <h3 class="text-donut">Carbon Emission Offset*</h3>
                    <h1 class="text-head-donut">3000 Kg</h1>
                    <h6>*When fully grown (in one year)</h6>
                </div>
                <div class="col-12 col-md-7 mt-4 mt-md-0 postion-relative">
					<doughnut-elem
                        class="postion-absolute"
                        style="z-index: 2; width: 100%; height: 100%;"
                        :labels="dataDonut2.labels"
                        :data="dataDonut2.data"
                        :backgroundColor="dataDonut2.backgroundColor"
                        :unit="dataDonut2.unit"
                        :text="dataDonut2.text"
                    ></doughnut-elem>
                </div>
            </div>

            <div style="height: 25vh;"></div>
            <div class="row">
                <div class="col-lg-5 offset-lg-1">
                    <carousel-slider></carousel-slider>
                </div>
                <div class="col-lg-4 text-bingsu-blue ml-lg-4">
                    <h2 style="font-size: 3.5rem; margin-bottom: 20px;">
                        Help us regrow the forest to offset your carbon
                        footprint!
                    </h2>
                    <a href="/donation_transaction"
                        ><donate-btn class="mt-4"></donate-btn
                    ></a>
                </div>
            </div>

            <!-- <div style="height: 20vh;"></div> -->

            <footer-phone></footer-phone>
        </div>
    </div>
</template>
<script>
import "~/assets/css/index.css";
import FooterPhone from "~/components/footer_phone.vue";
import CarouselSlider from "~/components/carousel_slider.vue";
import DonateBtn from "~/components/donate_button.vue"; // The donate button
import DoughnutElem from "~/components/doughnut_elem.vue";

export default {
    components: {
        FooterPhone,
        CarouselSlider,
        DonateBtn,
        DoughnutElem
    },
    layout: "main",
    data() {
        return {
            dataDonut: {
                labels: ["Robinhood", "Foodpanda", "Grab"],
                data: [250, 240, 250],
                backgroundColor: [
                    "rgba(108, 53, 142, 1)",
                    "rgba(215, 3, 101, 1)",
                    "rgba(68, 207, 95, 1)"
                ],
                unit: "kg of Carbon",
                text: "Carbon Emissions"
            },
			dataDonut2: {
                labels: ["Carbon adsorption", "Carbon left"],
                data: [250, 500],
                backgroundColor: [
                    'rgba(86, 215, 148, 1)',
					'rgba(0,0,0,0.1)'
                ],
                unit: "kg of Carbon",
                text: "Trees planted"
            },
            sections2: [
                { label: "Trees section", value: 32, color: "#56d794" }
            ],
            trees: 2498,
            totalCO2: 7809,
            modalTitle: "",
            modalCO2: ""
        };
    },
    methods: {
        handleSectionHover(section, event) {
            this.modalTitle = section.label;
            const indexFound = this.sections.findIndex(item => {
                return item.label == section.label;
            });
            this.modalCO2 =
                (this.totalCO2 * this.sections[indexFound].value) / 100;
            this.modalCO2 = parseInt(this.modalCO2);
            console.log(this.modalCO2);
        }
    }
};
</script>
