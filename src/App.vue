<template>
  <div>
    <div class="section">
      <div class="container">
        <div class="columns">
          <div class="column is-3 lista-de-conversas">
            <div class="barra-superior"></div>
            <div class="item" v-for="(conversa, index) in conversas" :key="index">
              <div class="title is-6">{{conversa.usuario}}</div>
              <div class="subtitle is-6">Ultima Mensagem...</div>
            </div>
          </div>
          <div class="column conversa-ativa">
            <div class="barra-superior">
              <span>Usuário</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import conversasIniciais from './conversasIniciais.js';

  export default {
    data: function() {
      return {
        conversas: conversasIniciais
      }
    }
  }
</script>


<style scoped>
  .columns {
    min-height:800px;
    box-shadow: 0 3rem 3rem -1rem rgba(10,10,10,.2);
  }

  .column {
    padding: 0;
  }

  .lista-de-conversas {
    background: white;
  }
  
  .conversa-ativa {
    background: #E5DDD5;
  }

  .barra-superior {
    margin: 0;
    height: 50px;
    background: #EDEDED;
    border-right: 1px solid #E1E1E1;
    border-bottom: 1px solid rgb(200, 200, 200);
  }

  .barra-superior span {
    line-height: 50px;
    margin-left: 25px;
    font-weight: 500;
  }

  .item {
    border-bottom: 1px solid #F2F2F2;
    padding: 15px 30px;
    margin-bottom: 0 !important;
  }

  .item:hover {
    background: #F5F5F5;
    cursor: pointer;
  }
</style>