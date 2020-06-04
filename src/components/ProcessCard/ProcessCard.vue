<template>
    <v-card class="mx-auto pa-2">
        <div class="d-flex">
            <v-avatar color="#328EBA" size="60" class="ma-2 avatarProcess">
            </v-avatar>
            <div class="mt-2">
                <p class="nameProcess">{{nameProcess}}</p>
                <p class="stage">{{stage}} Etapas</p>
            </div>
        </div>

        <v-divider></v-divider>
        <v-card-text class="pa-2 pt-0">
            <CardList/>
        </v-card-text>
        <v-card-actions :class="{'d-flex flex flex-column' :$vuetify.breakpoint.smAndDown}" >
            <v-spacer v-if="$vuetify.breakpoint.mdAndUp"></v-spacer>
            <v-btn text class="btnCardAction" color="#328EBA" :block="$vuetify.breakpoint.smAndDown">
                PRÉ-VISUALIZAR
            </v-btn>
            <v-btn class="btnCardAction white--text" color="#328EBA" :block="$vuetify.breakpoint.smAndDown">
                VER MENTORADOS
            </v-btn>
        </v-card-actions>
    </v-card>
</template>

<script>
    import CardList from "./CardList";

    export default {
        name: "ProcessCard",
        components: {
            CardList
        },
        props: {
            nameProcess: String,
            stage: Number

        }
    }
</script>

<style>
    .btnCardAction span {
        font-size: 14px;
        padding: 9px 16px;
    }

    .avatarProcess {
        border-radius: 50% !important;
    }

    .nameProcess {
        font-size: 16px;
        color: #424242;
        font-weight: bold;
    }

    .stage {
        font-size: 12px;
        color: #7F7F7F;
    }

    p.status {
        margin-bottom: 0 !important;
    }
</style>
