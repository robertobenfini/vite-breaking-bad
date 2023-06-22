<script>
export default {
    props:{
        myCard: Object
    }
}
</script>

<template>
    
    <img :src="myCard.imageUrl" alt="image" class="w-100">
    <h4>{{ myCard.name }}</h4>

</template>

<style lang="scss" scoped>

    

</style>