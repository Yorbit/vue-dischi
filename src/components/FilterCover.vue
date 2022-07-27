<template>
    <div>
        <label for="type">Seleziona il genere</label>
        <select name="type" id="type" v-model="selected"
            @change="$emit('search', selected)">
            <option value="jazz">Jazz</option>
            <option value="rock">Rock</option>
            <option value="metal">Metal</option>
            <option value="pop">Pop</option>
            <option value="all">All</option>
        </select>
    </div>
</template>

<script>
export default {
    data: function(){
        return{
            selected: '',
        }
    }
}
</script>


<style lang="scss" scoped>
    @import'../styles/colors.scss';
    div{
        align-self: baseline;
        position: relative;
        left: 1300px;
        top: -50px;
        label{
            text-transform: uppercase;
            font-weight: bold;
            color: black;
            padding-right: 15px
        }
        select{
            padding: 8px;
            text-transform: uppercase;
            font-weight: bold;
            option{
                text-transform: uppercase;
                font-weight: bold;
            }
        }
    }
</style>