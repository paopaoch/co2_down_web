<template>
    <div class="bg-tree">
        <div class="container-fluid">
            <div class="row">
                <div class="col-lg-6 col-md-11 offset-1 mb-4">
                    <div class="row" style="margin-top: 120px">
                        <div class="col-12">
                            <h1>Donate to offset your carbon emission</h1>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-lg-7 col-md-12 mt-2">
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
                        <div class="col-12 d-flex align-items-center">
                            <a href="/donation_transaction"
                                ><donate-btn></donate-btn
                                ><NuxtLink class="a-link ml-4" to="/donation_info"
                                    >Learn More
                                    <chev style="padding: 0 0 2px 0px;"></chev>
                                </NuxtLink>
                            </a>
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
    },
    data() {
        return {
            home: false,
            donation: true
        };
    }
};
</script>
