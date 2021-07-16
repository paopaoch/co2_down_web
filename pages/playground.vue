<template>
    <div class="test">
        <span :style="spanStyle" class="span1">hello world</span>
        <br>
        <span :style="{'--width': widthVar}" class="span2">hello earth</span>
    </div>
</template>
<script>
export default {
    data() {
        return {
            spanStyle: {
                "--color": "red"
            },
            widthVar: "100px"
        };
    }
}
</script>
<style scoped>
    .span1 {
        color: var(--color);
    }
    .span2 {
        text-align: center;
        position: relative;
        width: var(--width);
    }
    .span2::after {
        content: '';
        display: block;
        position: absolute;
        left: 100%; 
        width: var(--width);
        height: var(--width);
        border-radius: 50%;
        border: 2px solid black;      
    }
</style>
