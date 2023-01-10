<template>
    <div v-if="metge">
        <h1>{{ metge.nom }}</h1>
        h3>{{ metge.especialitat }}
    </div>
</template>

<script>
export default{
    props:['metge']
}
</script>