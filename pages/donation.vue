<template>
    <div class="bg-tree">
        <div class="container-fluid">
            <div class="row">
                <div class="col-6 offset-1">
                    <div class="row" style="margin-top: 120px">
                        <div class="col-12">
                            <h1>Donate to offset your carbon emission</h1>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-7 mt-2">
                            <p>
                                Each Kilometer travelled by delivey motorcycle
                                produce .... Kg of Greenhouse Gas, each Kilogram
                                of Greenhouse gas needs ... trees to offset its
                                damage on the planet. Help us achieve the 2030
                                agenda by donating to our Tree Planting today.
                            </p>
                        </div>
                    </div>
                    <div class="row mt-2">
                        <div class="col-2">
                            <a href="#"
                                ><donate-btn></donate-btn>
                            </a>
                        </div>
						<div class="col-4 d-flex align-items-center">
                            <NuxtLink class="a-link" to="/donation-info"
                                >Learn More <chev style="padding: 0 0 2px 0px;"></chev>
                            </NuxtLink>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import "~/assets/css/donation.css";
import DonateBtn from "~/components/donate_button.vue"; // The donate button
import Chev from "~/components/chev.vue"; // the chev icon

export default {
    layout: "main",
    components: {
        DonateBtn,
		Chev
    }
};
</script>
