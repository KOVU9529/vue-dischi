<template>
    <div class="section">     
      <div class="container">
          <div class="musicDisc" v-for="music,index in musicList" :key="index">
            <ComponentCard :music="music"/>
          </div>
      </div>
    </div>
</template>
<script>
import axios from "axios";
import ComponentCard from './ComponentCard.vue';
export default {
    name:'ListCard',
    components:{
        ComponentCard
    },
    data(){
        return{
            url:'https://flynn.boolean.careers/exercises/api/array/music ',
            musicList:[ ]
        }
    },
    created(){
        this.getMusic();
    },
    methods:{
        getMusic(){
            axios.get(this.url).then((result)=>{
                this.musicList=result.data.response
            });
        }
    }
}
</script>
<style lang="scss" scoped>
.section{
    height: 100vh;
}
.container{
    background-color: #1e2d3c;
    display: flex;
    flex-wrap: wrap;
    align-content: stretch;
    padding: 40px 350px;
    
   .musicDisc{
        width: calc((100% / 5) - 16px);
        margin: 0 8px;
    }
}
</style>
