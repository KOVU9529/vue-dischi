<template>
<!--Creo la select-->
  <div class="select">
      <!--Imposto l'azione @change per tracciare il cambiamento di valore della selct
          utilizzo emit per madare il messaggio 
          utilizzo la varaiabile genereFilter per tracciare i cambiamenti-->
      <select @change="$emit('changeGender',genereFilter)" v-model="genereFilter" id="selectGenre">
          <option  value="All">All</option>
          <option  value="Rock">Rock</option>
          <option  value="Jazz">Jazz</option>
          <option  value="Metal">Metal</option>
          <option  value="Pop">Pop</option>
      </select>
  </div>
</template>

<script>
export default {
    name:'SelectComponent',    
    data(){
        return{
            //imposto la variabile
            genereFilter:'',
        }
    }
}
</script>

.<style lang="scss" scoped>
.select{
    display: flex;
    justify-content: center;
    background-color: #1e2d3c;
    padding: 10px;
    #selectGenre{
        width:20% ;
        background-color: #2f3a47;
        border: none;
        border-radius: 20px;
        color: white;
        padding: 10px;
    }
}
</style>

