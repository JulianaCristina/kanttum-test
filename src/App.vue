<template>
    <v-app>
        <Toolbar/>
        <Sidebar/>
        <v-content class="wrapper">
            <PageHeader/>

            <v-row class="px-8">
                <v-col cols="12" md="6"v-for="(card, index) in cards" :key="index">
                    <ProcessCard  v-bind="card"/>
                </v-col>
            </v-row>
        </v-content>
    </v-app>
</template>

<script>
    import Toolbar from "./components/Toolbar/Toolbar";
    import Sidebar from "./components/Sidebar/Sidebar";
    import PageHeader from "./components/PageHeader/PageHeader";
    import ProcessCard from "./components/ProcessCard/ProcessCard";

    export default {
        name: 'App',

        components: {
            Toolbar,
            Sidebar,
            PageHeader,
            ProcessCard
        },

        data: () => ({
            cards: [
                {nameProcess: 'Teste', stage: 4},
                {nameProcess: 'Teste', stage: 5}
            ]
        }),
    };
</script>

<style>
    .wrapper{
        width: calc(100% - 100px);
        margin-left: 100px;
    }
</style>
