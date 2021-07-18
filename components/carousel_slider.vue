<template>
    <div>
        <b-carousel
            id="carousel-1"
            v-model="slide"
            :interval="4000"
            controls
            indicators
            background="#000000"
            img-width="1024"
            img-height="480"
            style="text-shadow: 1px 1px 2px #333;"
            @sliding-start="onSlideStart"
            @sliding-end="onSlideEnd"
        >
            <b-carousel-slide
                img-src="/slider/fotolia-92027264european-day-forest-green-forest.jpg"
            ></b-carousel-slide>

			<b-carousel-slide
                img-src="/slider/reforestacija-1024x682.jpg"
            ></b-carousel-slide>
			<b-carousel-slide
                img-src="/slider/Trees-1024x682.jpg"
            ></b-carousel-slide>
        </b-carousel>
    </div>
</template>

<script>
export default {
    data() {
        return {
            slide: 0,
            sliding: null
        };
    },
    methods: {
        onSlideStart(slide) {
            this.sliding = true;
        },
        onSlideEnd(slide) {
            this.sliding = false;
        }
    }
};
</script>
