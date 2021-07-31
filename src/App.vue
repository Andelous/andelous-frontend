<template>
    <v-app>
        <v-app-bar app class="grey darken-4">
            <v-app-bar-title>
                <router-link
                    to="/"
                    class="white--text"
                    style="text-decoration: none"
                >
                    <v-avatar>
                        <v-img
                            max-height="30"
                            max-width="30"
                            src="./assets/yo_small.jpg"
                        ></v-img>
                    </v-avatar>
                    <span class="font-weight-light">Angel</span
                    ><span class="teal--text font-weight-bold">D</span>
                </router-link>
            </v-app-bar-title>
        </v-app-bar>

        <v-main>
            <v-container fluid>
                <router-view />
            </v-container>
        </v-main>

        <v-footer
            app
            class="
                grey
                darken-2
                d-flex
                justify-space-between
                white--text
                font-weight-light
                pa-3
            "
            style="font-size: 0.8em"
        >
            <span>Angel Daniel Alonso Tovar</span>
            <span>Copyright &copy; {{ currentYear }}</span>
        </v-footer>
    </v-app>
</template>

<script>
export default {
    name: "App",

    data: () => ({
        currentYear: new Date().getFullYear(), //
    }),
};
</script>
