<template>
  <div>  
    <div class="card">
        <img  :src="music.poster" :alt="music.title">
        <div>{{music.title}}</div>
        <div class="text">
            <div class="color">{{music.author}}</div>
            <div class="color">{{music.year}}</div>            
        </div>

    </div>
  </div>
</template>
<script>
export default {
    name:'ComponentCard',
    props:['music']
}
</script>
<style lang="scss" scoped>
    .card{      
        padding: 10px;
        text-align: center;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: stretch;
        height: 250px;
        background-color: #2f3a47;
        margin-bottom: 10px;
        .text{
            display: flex;
            flex-direction: column;
             .color{
                color: #5b6368;
            }
        }
       
        img{
            width: 100%;
        }
    }
</style>>


