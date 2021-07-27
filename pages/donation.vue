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
                        <div class="col-lg-10 col-md-12 mt-2">
                            <p>
                                Each Kilometer travelled by a delivery
                                motorcycle produces around 110 g of Carbon
                                dioxide. Help us achieve Thailand’s 2030 agenda
                                to reduce gas emissions by 20%, by donating to
                                our Tree Planting project today. Every 20 Baht
                                donation will reward you with 5 Carbon Coins,
                                which you can exchange for rewards.
                            </p>
                        </div>
                    </div>
                    <div class="row mt-2">
                        <div class="col-12 d-flex align-items-center">
                            <span @click="postDonation()">
                                <donate-btn></donate-btn>
                            </span>
                            <NuxtLink
                                class="a-link ml-4 mb-1"
                                to="/donation_info"
                                >Learn More
                                <chev style="padding: 0 0 2px 0px;"></chev>
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
import axios from "axios";

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
    },
    methods: {
        async postDonation() {
            console.log("hello");
            const donation = await axios.post(
                "https://isvonshaljavzm4qc3g3xmwepm.appsync-api.ap-southeast-1.amazonaws.com/graphql",
                {
                    query: `mutation MyMutation {
					add_donation_trans(amount_baht: 50, user_id: "anonymous") {
					status
					}
				}
				`
                },
                {
                    headers: {
                        "x-api-key": process.env.API_KEY
                    }
                }
            );
            console.log(donation.data.data);
            // redirect('/donation_success')
            this.$router.push("/donation_success");
        }
    }
};
</script>
