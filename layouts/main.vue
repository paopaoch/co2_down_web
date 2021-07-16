<template>
    <div>
        <div>
            <b-navbar
                fixed="top"
                type="dark"
                toggleable="lg"
                style="background-color: transparent"
            >
                <div class="container-fluid">
                    <b-navbar-brand class="ml-3"
                        ><img src="/logo_version1.png" height="60px"
                    /></b-navbar-brand>

                    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                    <b-collapse id="nav-collapse" is-nav>
                        <b-navbar-nav>
                            <div v-if="$route.name == 'index'">
                                <b-nav-item href="#" active>Home</b-nav-item>
                            </div>
                            <div v-else>
                                <b-nav-item href="/">Home</b-nav-item>
                            </div>

							<div v-if="$route.name == 'donation' || $route.name == 'donation_info' || $route.name == 'donation_transaction'">
                                <b-nav-item href="/donation" active>Donation</b-nav-item>
                            </div>
                            <div v-else>
                                <b-nav-item href="/donation">Donation</b-nav-item>
                            </div>

							<div v-if="$route.name == 'about'">
                                <b-nav-item href="#" active>About Us</b-nav-item>
                            </div>
                            <div v-else>
                                <b-nav-item href="/about">About Us</b-nav-item>
                            </div>
                        </b-navbar-nav>

                        <b-navbar-nav class="ml-auto">
                            <button
                                class="btn btn-outline-success my-2 my-sm-0"
                                type="submit"
                            >
                                Get CO<sub>2</sub>l Down App
                            </button>
                        </b-navbar-nav>
                    </b-collapse>
                </div>
            </b-navbar>
        </div>
        <Nuxt />
    </div>
</template>
<script>
export default {
    data() {
        return {};
    }
};
</script>
