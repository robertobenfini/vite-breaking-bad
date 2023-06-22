<script>
export default {
    props:{
        myCard: Object
    }
}
</script>

<template>
    <div :class="myCard.type1 === 'Grass' ? 'bg-grass' : myCard.type1 === 'Fire' ? 'bg-fire' : myCard.type1 === 'Water' ? 'bg-water' : ''" class="card text-center d-flex align-items-center my-2">
        <img :src="myCard.imageUrl" alt="image">
        <div>{{ myCard.number }}</div>
        <div><h6>{{ myCard.name }}</h6></div>
        <div>{{ myCard.type1 }}</div>
    </div>

</template>

<style lang="scss" scoped>

    .bg-grass{
        background-color: #DEFDE0;
    }

    .bg-fire{
        background-color: #DEFDE0;
    }

    .bg-water{
        background-color: #DEF3FD;
    }

    img{
        height: 150px;
        width: 150px;
        border-radius: 50%;
        padding-top: 10px;
    }

</style>