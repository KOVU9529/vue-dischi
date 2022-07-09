<template>
  <div id="app">
    <HeaderComponent />
    <ListCard />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import ListCard from './components/ListCard.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    ListCard
  }
}
</script>

<style lang="scss">
 @import '@/assets/scss/style.scss';
 *{
    margin: 0%;
    padding: 0%;
    box-sizing: border-box;
  }

</style>
