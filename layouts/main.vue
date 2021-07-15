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
                            <b-nav-item href="/" active>Home</b-nav-item>

                            <b-nav-item-dropdown text="About us">
                                <b-dropdown-item
                                    class="news-dropdown-text"
                                    href="#"
                                    >Our vision</b-dropdown-item
                                >
                                <b-dropdown-item
                                    class="news-dropdown-text"
                                    href="#"
                                    >The Bingsu Team</b-dropdown-item
                                >
                            </b-nav-item-dropdown>

                            

                            <b-nav-item href="#">Contact us</b-nav-item>
							<b-nav-item href="/donation">Donation</b-nav-item>
                        </b-navbar-nav>

                        <b-navbar-nav class="ml-auto">
                            <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Get CO<sub>2</sub> l down</button>
                        </b-navbar-nav>
                    </b-collapse>
                </div>
            </b-navbar>
        </div>
        <Nuxt />

    </div>
</template>
<script>
import '~/assets/css/main.css';
export default {
};
</script>
