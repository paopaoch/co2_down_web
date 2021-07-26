<template>
    <div>
        <div>
            <b-navbar
                fixed="top"
                type="dark"
                toggleable="lg"
                style="background-color: rgba(76, 181, 149, 0.8)"
            >
                <div class="container-fluid">
                    <b-navbar-brand class="ml-3"
                        ><img src="/cooldown_logo.png" height="55"
                    /></b-navbar-brand>

                    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
                    <b-collapse id="nav-collapse" is-nav>
                        <b-navbar-nav>
                            <div v-if="$route.name == 'home'">
                                <b-nav-item href="#" active>Home</b-nav-item>
                            </div>
                            <div v-else>
                                <b-nav-item href="/home">Home</b-nav-item>
                            </div>

                            <div
                                v-if="
                                    $route.name == 'donation' ||
                                        $route.name == 'donation_info' ||
                                        $route.name == 'donation_transaction'
                                "
                            >
                                <b-nav-item href="/donation" active
                                    >Donation</b-nav-item
                                >
                            </div>
                            <div v-else>
                                <b-nav-item href="/donation"
                                    >Donation</b-nav-item
                                >
                            </div>
                            <div
                                v-if="
                                    $route.name == 'grab_page' ||
                                        $route.name == 'foodpanda_page' ||
                                        $route.name == 'robinhood_page'
                                "
                            >
                                <div>
                                    <b-nav-item-dropdown
                                        text="Weekly Report"
										class="active"
                                        right
                                    >
                                        <b-dropdown-item href="/grab_page"
                                            >Grab</b-dropdown-item
                                        >
                                        <b-dropdown-item href="/foodpanda_page"
                                            >Foodpanda</b-dropdown-item
                                        >
                                        <b-dropdown-item href="/robinhood_page"
                                            >Robinhood</b-dropdown-item
                                        >
                                    </b-nav-item-dropdown>
                                </div>
                            </div>
                            <div v-else>
                                <b-nav-item-dropdown text="Weekly Report">
                                    <b-dropdown-item href="/grab_page"
                                        >Grab</b-dropdown-item
                                    >
                                    <b-dropdown-item href="/foodpanda_page"
                                        >Foodpanda</b-dropdown-item
                                    >
                                    <b-dropdown-item href="/robinhood_page"
                                        >Robinhood</b-dropdown-item
                                    >
                                </b-nav-item-dropdown>
                            </div>
                            <div v-if="$route.name == 'about'">
                                <b-nav-item href="#" active
                                    >About Us</b-nav-item
                                >
                            </div>
                            <div v-else>
                                <b-nav-item href="/about">About Us</b-nav-item>
                            </div>
                        </b-navbar-nav>

                        <b-navbar-nav class="ml-auto">
                            <button
                                class="btn btn-outline-warning my-2 my-sm-0"
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
