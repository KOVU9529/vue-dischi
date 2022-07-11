<template>
  <div id="app">
    <HeaderComponent />
    <SelectComponent />
    <ListCard />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import ListCard from './components/ListCard.vue'
import SelectComponent from './components/SelectComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    ListCard,
    SelectComponent
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
