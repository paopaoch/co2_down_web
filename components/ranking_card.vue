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
						<ranking-elem rank="1" :name="ranks[0].name" :points="ranks[0].points"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="2" :name="ranks[1].name" :points="ranks[1].points" variant="primary"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="3" :name="ranks[2].name" :points="ranks[2].points" variant="danger"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="4" :name="ranks[3].name" :points="ranks[3].points" variant="warning"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="5" :name="ranks[4].name" :points="ranks[4].points" variant="success"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="6" :name="ranks[5].name" :points="ranks[5].points" variant="primary"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="7" :name="ranks[6].name" :points="ranks[6].points" variant="info"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="8" :name="ranks[7].name" :points="ranks[7].points"></ranking-elem>
					</div>
					<div class="col-lg-4 col-md-6 col-sm-12">
						<ranking-elem rank="9" :name="ranks[8].name" :points="ranks[8].points" variant="warning"></ranking-elem>
					</div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import RankingElem from "~/components/ranking_elem.vue";

export default {
	props: ['ranks'],
	components:{
		RankingElem
	}	
};
</script>
<style lang=""></style>
