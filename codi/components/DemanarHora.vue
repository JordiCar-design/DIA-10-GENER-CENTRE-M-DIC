<template>
<v-container>
    <v-row>
        <v-col>
            <EscollirMetge 
            @quanEscolleixiUnMetge="metgeEscollit()"
            ></EscollirMetge>
        </v-col>
        <v-col>
            <!-- <EscollirData></EscollirData> -->
        </v-col>
    </v-row>
</v-container>
</template>

<script>
export default{
    methods:{
        metgeEscollit(metge){
            console.log("s'ha escollit un metge..", metge)
        }
    }
}
</script>