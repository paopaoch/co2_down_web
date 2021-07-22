<template>
    <div class="bg-gradient pt-0">
        <div class="container">
            <div>
                <Logo />
                <!-- <h1 class="title">Bingsu</h1> -->
                <div class="links">
                    <a
                        href="#"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="button--grey"
                    >
                        Get the application
                    </a>
                    <a href="/home" class="button--grey">
                        Continue to Home
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import "~/assets/css/index.css";
export default {};
</script>

<style>
.container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.title {
    display: block;
    font-size: 5rem;
    color: #137785;
    letter-spacing: 1px;
}

.subtitle {
    font-size: 42px;
    color: #137785;
    word-spacing: 5px;
    padding-bottom: 15px;
}

.links {
    padding-top: 15px;
}
</style>
