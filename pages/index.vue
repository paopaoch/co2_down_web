<template>
    <div>
        <div class="container-fluid bg-gradient">
            <div class="row">
                <div class="col-3 offset-2">
                    <div>
                        <vc-donut
							v-b-modal.modal-center
                            background="#9fd4da"
                            :size="600"
                            unit="px"
                            :thickness="45"
                            :has-legend="false"
                            legend-placement="top"
                            :sections="sections"
                            :total="100"
                            :start-angle="0"
                            :auto-adjust-text-size="false"
                            @section-mouseover="handleSectionHover"
                            class="text-bingsu-blue"
                        >
                            <h5 class="text-donut">
                                Total CO<sub>2</sub> Emission
                            </h5>
                            <h2 class="text-head-donut">{{totalCO2}} kg</h2>
                        </vc-donut>
                    </div>
                </div>
                <div
                    class="col-3 offset-4 text-bingsu-blue"
					style="margin: auto;"
                >
                    <h3 class="text-donut">Season</h3>
					<h1 class="text-head-donut">July 2021</h1>
					<h3 class="text-donut">Users</h3>
					<h1 class="text-head-donut">2,498</h1>
					<h6>Look at weekly reports:</h6>
					<NuxtLink to="/grab_page">
						<img src="/logo/grab.jpg" width="80" alt="">
					</NuxtLink>

					<NuxtLink to="/foodpanda_page">
						<img class="mx-4" src="/logo/food_panda.png" width="80" alt="">
					</NuxtLink>
					
					<NuxtLink to="/robinhood_page">
						<img src="/logo/Robinhood-APK-MOD-Download-1.8.0.png" width="80" alt="">
					</NuxtLink>
					
                    <div>
                        <b-modal
                            id="modal-center"
                            centered
                            :title="modalTitle + ' CO2 Emission'"
                        >
                            <p class="my-4">{{ modalCO2 }} kg of carbon</p>
                        </b-modal>
                    </div>
                </div>
            </div>

            <div class="row mt-4">
                <div class="col-3 offset-2 my-auto text-bingsu-blue">
                    <h3 class="text-donut">Trees Planted</h3>
					<h1 class="text-head-donut">{{ trees }}</h1>
					<h3 class="text-donut"	>Carbon Emission Offset*</h3>
					<h1 class="text-head-donut">3000 Kg</h1>
					<h6>*When fully grown (in one year)</h6>
                </div>
                <div class="col-6">
                    <vc-donut
                        background="#a9d0e1"
                        :size="600"
                        unit="px"
                        :thickness="45"
                        :has-legend="false"
                        legend-placement="top"
                        :sections="sections2"
                        :total="100"
                        :start-angle="0"
                        :auto-adjust-text-size="false"
                        class="text-bingsu-blue"
                    >
                        <h5 class="text-donut">Trees planted</h5>
                        <h1 class="text-head-donut">{{ sections2[0].value }}%</h1>
                    </vc-donut>
                </div>
            </div>

			<div style="height: 25vh;"></div>
			<div class="row">
				<div class="col-5 offset-1">
					<carousel-slider></carousel-slider>	
				</div>
				<div class="col-4 text-bingsu-blue">
					<h2 style="font-size: 3.5rem; margin-bottom: 20px;">Help us regrow the forest to offset your carbon footprint!</h2>
					<a href="/donation_transaction"><donate-btn class="mt-4"></donate-btn></a>
				</div>
			</div>
			

            <div style="height: 20vh;"></div>

            <footer-phone></footer-phone>
        </div>
    </div>
</template>
<script>
import Donut from "vue-css-donut-chart";
import "vue-css-donut-chart/dist/vcdonut.css";
import Vue from "vue";
import "~/assets/css/index.css";
import FooterPhone from "~/components/footer_phone.vue";
import CarouselSlider from "~/components/carousel_slider.vue"
import DonateBtn from "~/components/donate_button.vue"; // The donate button

Vue.use(Donut);

export default {
    components: {
        FooterPhone,
		CarouselSlider,
		DonateBtn
    },
    layout: "main",
    data() {
        return {
            sections: [
                { label: "Robinhood", value: 35, color: "#6C358E"},
                { label: "Foodpanda", value: 30, color: "#d70365" },
                { label: "Grab", value: 35, color: "#44cf5f" }
            ],
            sections2: [
                { label: "Trees section", value: 32, color: "#56d794" }
            ],
			trees: 2498,
			totalCO2: 7809,
			modalTitle: '',
			modalCO2: ''
        };
    },
    methods: {
        handleSectionHover(section, event) {
			this.modalTitle = section.label
			const indexFound = this.sections.findIndex((item) => {
					return item.label == section.label
				})
			this.modalCO2 = this.totalCO2 * this.sections[indexFound].value / 100
			this.modalCO2 = parseInt(this.modalCO2)
			console.log(this.modalCO2)
        }
    }
};
</script>