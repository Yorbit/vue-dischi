<template>
  <header>
    <i class="bi bi-spotify"></i>
  </header>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
    @import'../../node_modules/bootstrap-icons/font/bootstrap-icons.css';
    @import'../styles/colors.scss';

    header{
        background-color: $headerBg;
        height: 90px;
        padding: 6px 30px;
        i{
          color: lightgreen;
          font-size: 70px;
        }
    }
</style>