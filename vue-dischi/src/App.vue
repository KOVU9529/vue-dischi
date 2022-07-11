<template>
  <div id="app">
    <HeaderComponent />
    <!---->
    <SelectComponent @changeGender="startSearch"/>
    <ListCard :activeFilter='activeGenre'/>
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
  },
  data() {
    return {
      activeGenre: 'All'
    }
  },
  methods:{
    //SETTO SEARCH FROM CHILD
    startSearch(genderToSearch){
      this.activeGenre = genderToSearch;
    }
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
