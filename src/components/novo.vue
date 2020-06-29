<template>
    <div id="adicionar">
        <input type="text" placeholder="Insira uma tarefa" class="adicionado" v-model="item"/>
        <button @click="enviarTexto()">Enviar</button>
    </div>
</template>

<script>
export default {
  name: "novo",
  props: ["tarefa"],
  data: function() {  
    return {
      item: "",
    };
  },
  methods: {
    enviarTexto: function() {
      this.$emit("AdicionarTexto", {
        item: this.item,
      });
    }
  }
};
</script>

<style>
#adicionar {
    width: 380px;
    height: 130px;
    border: 3px solid #ffffff;
    margin: 5px auto 0 auto;
    padding: 10px;
}

.adicionado {
    width: 150px;
    text-align: center;
    margin: 50px 10px 10px 90px;
}
</style>