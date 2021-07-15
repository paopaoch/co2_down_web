<template>
    <div class="bg-tree">
        <div class="container-fluid">
            <div class="row">
                <div class="col-6 offset-1">
                    <div class="row" style="margin-top: 120px">
                        <div class="col-12">
                            <h1>How Trees can reduce Carbon Emissions</h1>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-7 mt-2">
                            <p>
                                some description how trees can help, how many
                                tress needed to be plant, 2030 goal, how easy
                                and sustainable users can be bla bla..... ...
                                ...
                            </p>
                        </div>
                    </div>
                    <div class="row mt-2">
                        <div class="col-2">
                            <a href="https://www.google.com"
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
