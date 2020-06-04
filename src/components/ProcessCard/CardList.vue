<template>
    <v-container class="pa-0">
        <v-row >
            <v-expansion-panels flat>
                <v-expansion-panel v-for="(message, i) in messages" :key="i" hide-actions>
                    <v-expansion-panel-header disable-icon-rotate>
                        <v-row align="center" class="spacer pa-0" no-gutters>
                            <v-col cols="4" sm="2" md="1">
                                <v-avatar  size="36px">
                                    <v-icon color="#757575" v-text="message.icon"></v-icon>
                                </v-avatar>
                            </v-col>
                            <v-col class="text-no-wrap" cols="5" sm="3">
                                <strong>{{message.total}} {{message.title}}</strong>
                            </v-col>

                            <v-col class="text-no-wrap" cols="5" sm="3">
                                <p class="status">{{message.status}}</p>
                            </v-col>
                        </v-row>
                        <template v-slot:actions>
                            <v-icon color="#757575">mdi-chevron-right</v-icon>
                        </template>
                    </v-expansion-panel-header>

                    <v-expansion-panel-content>
                        <v-card-text v-text="lorem"></v-card-text>
                    </v-expansion-panel-content>
                    <v-divider></v-divider>
                </v-expansion-panel>
            </v-expansion-panels>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "CardList",
        data: () => ({
            messages: [
                {
                    icon: 'mdi-school',
                    total: 102,
                    title: 'atividades',
                    status: 'aguardando mentoria'
                },
                {
                    icon: 'mdi-video',
                    total: 9,
                    title: 'evidências',
                    status: 'aguardando mentoria'
                },
                {
                    icon: 'mdi-account-voice',
                    total: 4,
                    title: 'feedback',
                    status: 'aguardando mentoria'
                },
            ],
            lorem: 'Lorem ipsum dolor sit amet, at aliquam vivendum vel, everti delicatissimi cu eos. Dico iuvaret debitis mel an, et cum zril menandri. Eum in consul legimus accusam. Ea dico abhorreant duo, quo illum minimum incorrupte no, nostro voluptaria sea eu. Suas eligendi ius at, at nemore equidem est. Sed in error hendrerit, in consul constituam cum.',
        }),
    }
</script>

<style >
    .v-expansion-panel-header{
        padding: 16px 8px;
    }
    .status{
        color: #7F7F7F;
        font-size: 14px;
    }
</style>
