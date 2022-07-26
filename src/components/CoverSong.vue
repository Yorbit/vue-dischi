<template>
    <div class="cover">
        <div class="image-container">
            <img :src="imageUrl" alt="">
        </div>
        <h3>{{ title }}</h3>
        <p>{{ author }}</p>
        <p>{{ year }}</p>
    </div>
</template>

<script>
export default {
    props: {
        imageUrl: String,
        title: String,
        author: String,
        year: String,
    }
}
</script>

<style lang="scss" scoped>
    @import'../styles/colors.scss';
    .card{
        background-color: $covers;
        width: calc(100% / 5 - 30px);
        height: 320px;
        text-align: center;
        margin-bottom: 20px;
        margin-right: 30px;
        padding: 20px;
        img {
                object-fit: cover;
                width: 100%;
            }
        h3{
            color: white;
            text-transform: uppercase;
            margin: 5px 0px;
            font-weight: bold;
        }
        p{
            color: $textCovers;
        }     
    }
</style>