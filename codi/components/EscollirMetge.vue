<template>
<div>
            <!-- <Metge
        v-for="item in metges"
        :elMetge="item"
        >
    </Metge> 
    </div> -->

    <div @click="seleccionarMetge(pos)"
        class="metgeClass" v-for="(item, pos) in metges"
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
                    nom:"Dr. P",
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
        seleccionarMetge(metge)
        {
            console.log('metge seleccionat', this.metges[posicio])
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
    background-color: antiquewhite;
    cursor: pointer;

}
</style>