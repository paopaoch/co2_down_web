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
                        <div class="col-lg-11 col-md-12 mt-2">
                            <p>
                                Trees can offset Carbon Emissions by absorbing
                                it and produce Oxygen in return. Trees also
                                contribute to lowering the global temperature,
                                which is one of our urgent climate challenges.
                                In a year, a fully grown tree can absorb around
                                9-15 Kg of Carbon Dioxide. We aim to reduce and
                                offset the Carbon emission per capita, which in
                                2020 was 3.68 Tons. To offset that amount we
                                need 307 trees per person in Thailand each year.
                                Donate to our Tree Planting project to make this
                                goal a reality.
                            </p>
                        </div>
                    </div>
                    <div class="row mt-2">
                        <div class="col-4">
                            <span @click="postDonation()">
                                <donate-btn></donate-btn>
                            </span>
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
