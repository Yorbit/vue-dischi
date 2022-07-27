<template>
    <div class="cover">
        <div class="image-container">
            <img :src="imageUrl" alt="">
        </div>
        <p>{{ type }}</p>
        <h3>{{ title }}</h3>
        <p>{{ author }}</p>
        <p>{{ year }}</p>
    </div>
</template>

<script>
export default {
    props: {
        imageUrl: String,
        type: String,
        title: String,
        author: String,
        year: String,
    }
}
</script>

<style lang="scss" scoped>
    @import'../styles/colors.scss';
    .cover{
        background-color: $headerCoverBg;
        text-align: center;
        width: calc(100% / 5 - 50px);
        height: 350px;
        padding: 10px;
        margin-bottom: 30px;
        margin-right: 25px;
        img {
                object-fit: cover;
                width: 100%;
            }
        h3{
            color: white;
            margin: 5px 0px;
            font-weight:500;
            text-transform: uppercase;
        }
        p{
            color: $textCovers;
        }     
    }
</style>