<script>
export default {
    props:{
        myCard: Object
    },
    computed:{
        getColor(){
            return this.myCard.color.toLowerCase();
        }
    }
}
</script>

<template>
    <div class="card text-center d-flex align-items-center my-2" :style="{'background-color':getColor}">
        <img :src="myCard.imageUrl" alt="image">
        <div>{{ myCard.number }}</div>
        <div><h6>{{ myCard.name }}</h6></div>
        <div>{{ myCard.type1 }}</div>
    </div>

</template>

<style lang="scss" scoped>

    img{
        height: 150px;
        width: 150px;
        border-radius: 50%;
        padding-top: 10px;
    }

</style>