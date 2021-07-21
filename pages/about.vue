<template>
    <div class="bg-gradient">
        <div class="container">
            <div class="row mb-4">
                <div class="col-12 col-md-4 offset-md-4 text-center">
                    <h1 class="text-espresso-blue">Our Mission</h1>
                    <hr
                        class="mt-1 bg-espresso-blue"
                        width="200px"
                        style="margin: auto; height: 0.5px"
                    />
                </div>
            </div>
            <div class="row mb-4">
                <div class="col-12">
                    <div
                        class="card"
                        style="width: 100%; border-radius: 20px; background-color: rgba(0, 0, 0, 0.1);"
                    >
                        <div class="card-body text-white">
                            <p>
                                Amidst the growing concerns and risks associated
                                with climate change, Collective Climate Action
                                has become a priority as illustrated through
                                Thailand’s goal to reduce greenhouse gas (GHG)
                                emissions by 20% by 2030. Nonetheless, the
                                majority of Thai society lack the knowledge and
                                incentive to reduce their carbon footprint.
                            </p>
                            <p>
                                Perpetuated by COVID-19 and consequent WFH
                                practices, this influenced consumption habits
                                resulting in more frequent yet inefficient
                                online food orders. With the transport sector
                                being one of the top contributors to the
                                sustained increased in carbon emissions and
                                energy consumption in the country, the lack of
                                societal awareness and the transportation’s
                                rising contribution to carbon emissions
                                emphasize how these two factors should be
                                addressed as a way to combat climate change.
                            </p>
                            <p>
                                Studies highlighted that without structural and
                                technological innovations, further GHG emission
                                reduction targets would merely create greater
                                challenges to Thailand’s energy and economic
                                systems, and ultimately lead to greater GDP and
                                welfare losses. In the face of globalization, it
                                is crucial to address this problem before the
                                consequences offset the potential for future
                                economic development and individuals’
                                well-being.
                            </p>
                            <p>
                                CO<sub>2</sub>l Down would like to see a world
                                where nature and modern technology live together
                                in harmony, where everyone is aware of their
                                carbon foot print and colaborate in improving
                                the world one small bit at a time.
                            </p>
                            <h6>
                                Lets cool down the earth in a cool way with
                                CO<sub>2</sub>l Down!
                            </h6>
                            <p class="text-light my-4">
                                - The team at CO<sub>2</sub>l Down
                            </p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row my-4">
                <div
                    class="col-12 col-md-4 offset-md-4 text-center"
                    style="margin-top: 50px"
                >
                    <h1 class="text-espresso-blue">The Team</h1>
                    <hr
                        class="mt-1 bg-espresso-blue"
                        width="180px"
                        style="margin: auto; height: 0.5px"
                    />
                </div>
            </div>
            <div class="row d-none d-lg-flex">
                <div class="col-lg-4">
                    <team-card
                        img="/members/paopao.jpg"
                        name="Chulabutra (PaoPao) Chuenchoksan"
                        role="Web and Backend Developer"
                    ></team-card>
                </div>
                <div class="col-lg-4 d-flex justify-content-center">
                    <team-card
                        img="/members/egai2.jpg"
                        name="Nicharee (Yumiko) Suwannaroj"
                        role="Front-end App Developer"
                    ></team-card>
                </div>
                <div class="col-lg-4 d-flex justify-content-end">
                    <team-card
                        img="/members/chap.jpg"
                        name="Chanop (Chap) Sethiwan"
                        role="Cloud Admin and Backend Developer"
                    ></team-card>
                </div>
            </div>
            <div class="row d-none d-lg-flex py-4">
                <div class="col-lg-4 offset-lg-2 d-flex justify-content-start">
                    <team-card
                        img="/members/grace.jfif"
                        name="Chatchamol (Grace) Anantaprayoon"
                        role="Business Analyst and UI Designer"
                    ></team-card>
                </div>
                <div class=" col-lg-4 d-flex justify-content-end">
                    <team-card
                        img="/members/mim.jpg"
                        name="Nathatai (Mim) Saraya"
                        role="Business Analyst and UI Designer"
                    ></team-card>
                </div>
            </div>

            <div class="row d-none d-md-flex d-lg-none">
                <div class="col-6 d-flex justify-content-center">
                    <team-card
                        img="/members/paopao.jpg"
                        name="Chulabutra (PaoPao) Chuenchoksan"
                        role="Web and Backend Developer"
                    ></team-card>
                </div>
                <div class="col-6 d-flex justify-content-center">
                    <team-card
                        img="/members/egai2.jpg"
                        name="Nicharee (Yumiko) Suwannaroj"
                        role="Front-end App Developer"
                    ></team-card>
                </div>
            </div>
            <div class="row d-none d-md-flex d-lg-none mt-4">
                <div class="col-12 d-flex justify-content-center">
                    <team-card
                        img="/members/chap.jpg"
                        name="Chanop (Chap) Sethiwan"
                        role="Cloud Admin and Backend Developer"
                    ></team-card>
                </div>
            </div>
            <div class="row d-none d-md-flex d-lg-none py-4">
                <div class="col-6 d-flex justify-content-center">
                    <team-card
                        img="/members/grace.jfif"
                        name="Chatchamol (Grace) Anantaprayoon"
                        role="Business Analyst and UI Designer"
                    ></team-card>
                </div>
                <div class="col-6 d-flex justify-content-center">
                    <team-card
                        img="/members/mim.jpg"
                        name="Nathatai (Mim) Saraya"
                        role="Business Analyst and UI Designer"
                    ></team-card>
                </div>
            </div>

            <div class="row d-sm-flex d-md-none mb-4">
                <div class="col-12 d-flex justify-content-center">
                    <team-card
                        img="/members/paopao.jpg"
                        name="Chulabutra (PaoPao) Chuenchoksan"
                        role="Web and Backend Developer"
                    ></team-card>
                </div>
            </div>

			<div class="row d-sm-flex d-md-none mb-4">
                <div class="col-12 d-flex justify-content-center">
                    <team-card
                        img="/members/egai2.jpg"
                        name="Nicharee (Yumiko) Suwannaroj"
                        role="Front-end App Developer"
                    ></team-card>
                </div>
            </div>

			<div class="row d-sm-flex d-md-none mb-4">
                <div class="col-12 d-flex justify-content-center">
                    <team-card
                        img="/members/chap.jpg"
                        name="Chanop (Chap) Sethiwan"
                        role="Cloud Admin and Backend Developer"
                    ></team-card>
                </div>
            </div>

			<div class="row d-sm-flex d-md-none mb-4">
                <div class="col-12 d-flex justify-content-center">
                    <team-card
                        img="/members/grace.jfif"
                        name="Chatchamol (Grace) Anantaprayoon"
                        role="Business Analyst and UI Designer"
                    ></team-card>
                </div>
            </div>

			<div class="row d-sm-flex d-md-none">
                <div class="col-12 d-flex justify-content-center">
                    <team-card
                        img="/members/mim.jpg"
                        name="Nathatai (Mim) Saraya"
                        role="Business Analyst and UI Designer"
                    ></team-card>
                </div>
            </div>
            
            <footer-phone style="margin-top: 200px"></footer-phone>
        </div>
    </div>
</template>
<script>
import "~/assets/css/index.css";
import "~/assets/css/about.css";
import TeamCard from "~/components/team_card.vue";
import FooterPhone from "~/components/footer_phone.vue";

export default {
    layout: "main",
    components: {
        TeamCard,
        FooterPhone
    }
};
</script>
