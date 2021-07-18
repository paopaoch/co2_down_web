<template>
    <div>
        <b-list-group-item
            class="my-2 d-flex align-items-center rounded border-0"
            style="background: rgba(0,0,0,0.2);"
        >
            <h5 class="my-auto mx-2">{{rank}}.</h5>
            <b-avatar
                :variant="variant"
                :src="src"
                class="mr-3"
            ></b-avatar>
            <span class="mr-auto">{{name}}</span>
            <b-badge>{{points}}</b-badge>
        </b-list-group-item>
    </div>
</template>
<script>
export default {
	
	props: ['src', 'rank', 'name', 'points', 'variant'],
};
</script>
<style></style>
