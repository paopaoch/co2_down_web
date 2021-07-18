<template>
    <div class="bg-tree">
        <div class="container-fluid">
            <div class="row">
                <div class="col-lg-6 col-md-11 offset-1 mb-4">
                    <div class="row" style="margin-top: 120px">
                        <div class="col-12">
                            <h1>How Trees can reduce Carbon Emissions</h1>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-lg-7 col-md-12 mt-2">
                            <p>
                                some description how trees can help, how many
                                tress needed to be plant, 2030 goal, how easy
                                and sustainable users can be bla bla..... ...
                                ...
                            </p>
                        </div>
                    </div>
                    <div class="row mt-2">
                        <div class="col-4">
                            <a href="/donation_transaction"
                                ><donate-btn></donate-btn>
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
    }
};
</script>
