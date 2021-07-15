<template>
    <div>
        <div class="card" style="width: 18rem; border-radius: 20px; min-height: 380px; background-color: rgba(0, 0, 0, 0.2);">
            <div class="card-body text-center">
                <div class="d-flex justify-content-center my-4">
                    <img
                        class="rounded-circle"
                        :src="img"
                        alt=""
                        width="200"
						height="200"
                    />
                </div>

                <h5 class="card-title text-white">{{ name }}</h5>
                <h6 class="card-subtitle mb-2 text-light">
                    {{ role }}
                </h6>
            </div>
        </div>
    </div>
</template>
<script>
export default {
	props: ['name', 'img', 'role']
};
</script>
<style></style>
