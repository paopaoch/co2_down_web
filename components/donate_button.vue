<template>
    <button class="btn btn-donate">
        <span class="pl-1">Donate</span
        ><chev style="padding: 0 0 2px 15px;"></chev>
    </button>
</template>
<script>
import Chev from "~/components/chev.vue";

export default {
	components: {
		Chev
	}
}
</script>
<style>
.btn-donate {
    background-color: #11253e;
    border-radius: 20px;
    display: inline-block;
    cursor: pointer;
    color: #ffffff;
    font-family: Arial;
    font-size: 1rem;
	width: 110px;
    padding: 4px 10px;
    text-decoration: none;
}
.btn-donate:hover {
    background-color: #050a11;
	color: white;
}
.btn-donate:active {
    position: relative;
    top: 1px;
}

</style>