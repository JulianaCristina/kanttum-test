<template>
    <div class="pageHeader px-8">
        <p>Formação</p>

        <v-btn text>
            <v-icon color="#E1E1E1">mdi-dots-vertical</v-icon>
        </v-btn>
    </div>
</template>

<script>
    export default {
        name: "PageHeader"
    }
</script>

<style>
    .pageHeader {
        background: #FAFAFA;
        height: 89px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .pageHeader p {
        font-size: 24px;
        font-weight: bold;
        color: #424242;
    }

</style>
