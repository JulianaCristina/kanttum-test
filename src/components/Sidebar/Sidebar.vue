<template>
    <v-navigation-drawer app class="sidebar" permanent color="#F5F5F5" width="100px">
        <v-divider></v-divider>
        <v-list height="65px">
            <v-list-item v-for="item in items" :key="item.title" link>
                <v-list-item-content>
                    <v-icon class="iconList">{{ item.icon }}</v-icon>
                    <v-list-item-title class="menuTitle mb-1">{{ item.title }}</v-list-item-title>
                </v-list-item-content>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
    export default {
        name: "Sidebar",
        data() {
            return {

                items: [
                    {title: 'Formações', icon: 'mdi-chart-donut'},
                    {title: 'Cursos', icon: 'mdi-school'},
                    {title: 'Canais', icon: 'mdi-play-circle-outline'},
                    {title: 'Relatórios', icon: 'mdi-poll'},
                    {title: 'Grupos de Usuários', icon: 'mdi-account-supervisor'},
                ],
                mini: true,
            }
        },
    }
</script>

<style>
    .sidebar {
        top: 64px !important;
    }

    .menuTitle {
        text-align: center;
        white-space: normal!important;
        font-size: 13px !important;
    }
    .v-navigation-drawer__border{
        background-color: #FAFAFA!important;
    }
    .v-list-item{
        padding: 0!important;
    }
    .iconList{
        margin-bottom: 5px!important;
    }

</style>
