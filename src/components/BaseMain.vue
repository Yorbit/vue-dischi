<template>
  <main>
    <FilterCover @search="filterCover"/>
    <div class="container" v-if="(songs.length == 10)">
        <CoverSong v-for="(song, index) in filteredCoverType" :key="index" 
            :imageUrl="song.poster"
            :type="song.type"
            :year="song.year"
            :title="song.title"
            :author="song.author"
        />
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import CoverSong from "./CoverSong.vue";
import FilterCover from "./FilterCover.vue";

export default {
    data: function(){
        return{
            songs: [],
            filteredCoverType: [],
        }
    },
    components: {
    CoverSong,
    FilterCover,
},

      methods: {
        getSong(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((result) => {
                this.songs = result.data.response;
                this.filteredCoverType = this.songs;
            })
        },
        filterCover(selected){
            this.filteredCoverType = [...this.songs].filter( (song) => song.genre.toLowerCase().includes(selected));
            console.log(this.filteredCoverType);
            
            if (selected == 'all') {
                this.filteredCoverType = this.songs;
            }
        },
    },
    created(){
            setTimeout(() => this.getSong(), 100);
    }
}
</script>

<style lang="scss" scoped>
    @import'../styles/colors.scss';

    main{
        background-color: $headerMn;
        height: calc(100vh - 90px);
        justify-content: center;
        align-items: center;
        display: flex;
        .container{
          display: flex;
          flex-wrap: wrap;
          width: 70%;
        }
    }
</style>