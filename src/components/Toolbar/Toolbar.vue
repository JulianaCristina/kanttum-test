<template>

    <v-app-bar app
               color="#2B8FBA"
               height="64px"
               extension-height=0
               class="bar ma-0"
               flat
    >
        <v-btn text height="64px" width="100px">
            <v-img :src="require('../../assets/img/icon-kanttum.svg')" contain ></v-img>
        </v-btn>
        <v-spacer></v-spacer>

        <v-btn icon class="mr-5">
            <v-badge
                    :content="messages"
                    :value="messages"
                    class="badgeIcon"
                    color="red"
                    overlap

            >
                <v-icon size="24" color="#55A5C8">mdi-bell</v-icon>
            </v-badge>
        </v-btn>

        <v-menu left>
            <template #activator="{on}">
                <v-btn
                        icon
                        class="mr-5 profile"

                >
                    <v-img :src="require('../../assets/img/user-profile.png')" contain v-on='on' height="36"
                           width="36"/>
                    <v-icon size="24" color="#55A5C8">mdi-menu-down</v-icon>
                </v-btn>
            </template>
        </v-menu>
    </v-app-bar>

</template>

<script>
    export default {
        name: "Toolbar",
        data() {
            return {
                messages: 1,
                show: true,

            }
        },

    }
</script>

<style>
    .bar .v-toolbar__content{
        padding-left: inherit;
    }
    .profile:hover{
        color: transparent!important;
    }
</style>
