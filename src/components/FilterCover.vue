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
