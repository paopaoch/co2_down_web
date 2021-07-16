<template>
    <div>
        <button
            class="btn button-full d-flex justify-content-start align-items-center"
            v-bind:style="{
                backgroundImage:
                    'linear-gradient(' + color + ',' + color +'), url(' +
                    image +
                    ')',
                backgroundPosition: 'center center',
                backgroundSize: 'cover',
                backgroundRepeat: 'no-repeat',
				margin: '0'
            }"
        >
            <span class="text-light button-text ml-4" style="min-width: 42%;">{{ text }}</span>
            <span class="verticle-line align-self-center"></span>
			<span class="text-light button-text ml-4">{{ price }}฿</span>
        </button>
    </div>
</template>
<script>
export default {
    props: ["image", "text", "price", "color"]
};
</script>
<style>
.button-full {
    height: 100%;
    width: 100%;
    border-radius: 50px;
}

.button-text {
    font-size: 2rem;
}

.verticle-line {
    border-right: 2px solid white;
    height: 50%;
}
</style>
