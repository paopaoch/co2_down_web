<template lang="">
    <div>
        <div
            class="card mt-4"
            style="width: 100%; border-radius: 20px; background-color: rgba(0, 0, 0, 0.1);"
        >
            <div class="card-body">
                <div class="row">
                    <div class="col-4 d-flex justify-content-center">
                        <h3 class="text-white">Top Players Last Week</h3>
                    </div>
                </div>
                <div class="row text-white">
                    <div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="1" name="Sakupao" points="4202"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="2" name="Grace_a" points="4110" variant="primary"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="3" name="yumi-mosa" points="4105" variant="danger"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="4" name="DelG" points="4026" variant="warning"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="5" name="MimImiM" points="3500" variant="success"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="6" name="mosa-yumi" points="3456" variant="primary"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="7" name="Sakupao2" points="3234" variant="info"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="8" name="ENae" points="3156"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="9" name="GaiGinKo" points="3048" variant="warning"></ranking-elem>
					</div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import RankingElem from "~/components/ranking_elem.vue";

export default {
	components:{
		RankingElem
	}	
};
</script>
<style lang=""></style>
