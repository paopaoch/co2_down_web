<template>
    <div class="bg-tree">
        <div class="container-fluid">
            <div class="row">
                <div class="col-lg-6 col-md-11 offset-1">
                    <div class="row" style="margin-top: 120px">
                        <div class="col-12">
                            <h1>Choose your tree</h1>
                        </div>
                    </div>

                    <div class="row">
                        <div class="col-lg-7 col-md-12 mt-2 ml-4">
                            <p>
                                Choose the tree you would like to donate. To
                                gain the most from your donation download our
                                application first to get Carbon Coins for
                                discount vouchers from top delivery apps!
                            </p>
                        </div>
                    </div>

                    <div class="row mt-2">
                        <div class="col-5">
                            <donation-card
                                image="/willow.png"
                                style="height: 100px; width: 300px"
                                text="Willow"
                                price="200"
                                color="rgba(0,0,0, 0.5)"
                            ></donation-card>
                        </div>
                    </div>
                    <div>
                        <div class="row">
                            <div class="col-5 my-4">
                                <donation-card
                                    image="/oak.png"
                                    style="height: 100px; width: 300px"
                                    text="Oak"
                                    price="100"
                                    color="rgba(0,0,0, 0.5)"
                                ></donation-card>
                            </div>
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
import DonationCard from "~/components/donation_card.vue";

export default {
    layout: "main",
    components: {
        DonateBtn,
        Chev,
        DonationCard
    }
};
</script>
