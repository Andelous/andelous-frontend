<template>
    <div>
        <v-row>
            <v-col cols="12" sm="8">
                <h2 class="mb-4">Who am I&quest;</h2>
                <p>
                    My name is Angel, but you can call me by my pseudonym,
                    <strong>Andelous</strong>. I built this page just for the
                    sake of fun. I hope you like what you see.
                </p>
                <p>
                    Here you can see some of the skills I have, the tools I work
                    with, and some sample apps that I've created
                    <code>;)</code>.
                </p>

                <h3 class="mb-4">A little about me</h3>

                <p>
                    I grew up in Oaxaca, Mexico, studied Software Engineering
                    and now I'm here. I like to develop applications from
                    scratch&#59; the thought process to come up with solutions,
                    studying the tools, and figuring out how to solve the
                    emergent problems make me passionate about this major.
                </p>

                <p>
                    I also like chess
                    <v-icon color="black" small>mdi-chess-pawn</v-icon> and
                    videogames
                    <v-icon color="black" small
                        >mdi-microsoft-xbox-controller</v-icon
                    >.
                </p>
            </v-col>
            <v-col cols="12" sm="4">
                <h2 class="mb-4">Quick access</h2>

                <template v-for="linkSection in linkSections">
                    <link-section
                        v-bind:title="linkSection.title"
                        v-bind:links="linkSection.links"
                        v-bind:key="linkSection.title"
                    />
                    <br v-bind:key="linkSection.title + 'br'" />
                </template>
            </v-col>
        </v-row>

        <v-divider class="my-4" />

        <v-row>
            <v-col cols="12">
                <div class="d-flex justify-start align-center">
                    <v-icon color="teal darken-2">mdi-cog</v-icon>
                    <span>&nbsp;&nbsp;</span>
                    <h2>Technologies I use</h2>
                </div>
            </v-col>
        </v-row>

        <v-row>
            <v-col
                cols="6"
                sm="3"
                lg="2"
                class="text-center"
                v-for="tech in technologies"
                v-bind:key="tech.icon"
            >
                <avatar-icon
                    v-bind:icon="tech['icon']"
                    v-bind:avatar-color="tech['avatar-color']"
                    v-bind:icon-color="tech['icon-color']"
                    v-bind:avatar-size="tech['avatar-size']"
                    v-bind:icon-size="tech['icon-size']"
                />
            </v-col>
        </v-row>
    </div>
</template>

<script>
import AvatarIcon from "../components/AvatarIcon.vue";
import LinkSection from "../components/LinkSection.vue";

export default {
    name: "Home",

    components: { "avatar-icon": AvatarIcon, "link-section": LinkSection },

    data: () => ({
        technologies: [
            {
                icon: "mdi-microsoft-azure",
                "avatar-color": "white",
                "icon-color": "blue darken-2",
                "avatar-size": "6em",
                "icon-size": "5em",
            },
            {
                icon: "mdi-language-java",
                "avatar-color": "white",
                "icon-color": "red darken-2",
                "avatar-size": "6em",
                "icon-size": "5em",
            },
            {
                icon: "mdi-language-javascript",
                "avatar-color": "white",
                "icon-color": "yellow accent-4",
                "avatar-size": "6em",
                "icon-size": "5em",
            },

            {
                icon: "mdi-database-outline",
                "avatar-color": "white",
                "icon-color": "grey",
                "avatar-size": "6em",
                "icon-size": "5em",
            },
        ],
        linkSections: [
            {
                title: "Professional",
                links: [
                    {
                        target: "_blank",
                        href:
                            "https://mx.linkedin.com/in/angel-daniel-alonso-tovar",
                        icon: "mdi-linkedin",
                        "icon-color": "blue darken-3",
                        text: "LinkedIn",
                    },
                    {
                        target: "_blank",
                        href: "https://github.com/Andelous",
                        icon: "mdi-github",
                        "icon-color": "black",
                        text: "GitHub",
                    },
                ],
            },
            {
                title: "Sample apps",
                links: [
                    {
                        href: "#",
                        icon: "mdi-check",
                        "icon-color": "red",
                        text: "Sample app 1",
                    },
                    {
                        href: "#",
                        icon: "mdi-clipboard",
                        "icon-color": "green darken-2",
                        text: "Sample app 2",
                    },
                    {
                        href: "#",
                        icon: "mdi-cog",
                        "icon-color": "blue darken-2",
                        text: "Sample app 3",
                    },
                ],
            },
            {
                title: "Want to play?",
                links: [
                    {
                        target: "_blank",
                        href: "https://www.chess.com/member/andelous",
                        icon: "mdi-chess-pawn",
                        "icon-color": "green darken-3",
                        text: "Chess.com",
                    },
                    {
                        target: "_blank",
                        href:
                            "https://steamcommunity.com/profiles/76561197999789497",
                        icon: "mdi-steam",
                        "icon-color": "blue-grey darken-3",
                        text: "Steam",
                    },
                ],
            },
        ],
    }),
};
</script>
