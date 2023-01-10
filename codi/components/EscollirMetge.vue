<template>
<div>
            <!-- <Metge
        v-for="item in metges"
        :elMetge="item"
        >
    </Metge> 
    </div> -->

        <div @click="seleccionarMetge(pos)" 
        class="metge" v-for="(item, pos) in metges"
            :key="pos">
            <strong>{{ item.nom }}</strong>
            <br>
            {{ item.especialitat }}
    </div>
</div>
</template>

<script>
export default {
    data(){
        return{
            metges:[
                {
                    nom:"Dr. Tal",
                    especialitat:"Traumatologia"
                },
                {
                    nom:"Dr. Qual",
                    especialitat:"Medicina General"
                },
                {
                    nom:"Dr. Fulano",
                    especialitat:"Pediatria"
                },
                {
                    nom:"Dr. Sutano",
                    especialitat:"Cardiologia"
                }
            ]
        }
    },
    methods:{
        seleccionarMetge(posicio)
        {
            console.log('metge seleccionat', this.metges[posicio])

            this.$emit('quanEscolleixiUnMetge')
        }
    }
}
</script>

<style scoped>

h2{
    font-size:5000px;
}

.metge{
    margin:5px;
    padding:5px;
    background-color: red;
    cursor: pointer;

}
</style>