<template>
    <div class="bg-tree">
        <div class="container-fluid">
            <div class="row">
                <div class="col-lg-6 col-md-11 offset-1 mb-4">
                    <div class="row" style="margin-top: 120px">
                        <div class="col-12">
                            <h1>Donation Success!</h1>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-lg-11 col-md-12 mt-2">
                            <p>
                                Thanks for your donation! Your donation means
                                that our earth can CO<sub>2</sub>l down a
                                little. Now its time to download our application
                                to track your delivery habits!
                            </p>
                        </div>
                    </div>
                    <div class="row mt-2">
                        <div class="col-4">
                            <NuxtLink to="/"
                                ><button
                                    class="btn btn-warning my-2 my-sm-0"
                                    type="submit"
                                >
                                    Get CO<sub>2</sub>l Down App
                                </button></NuxtLink
                            >
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
import "~/assets/css/index.css";

export default {
    layout: "main",
    components: {
        DonateBtn,
        Chev
    }
};
</script>
