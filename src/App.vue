<template>
    <div id="app">
        <novo :tarefa="tarefa" @AdicionarTexto="adicionar($event)"/>
        <coisas :tarefa="tarefa" />
    </div>
</template>

<script>
import novo from "./components/novo.vue";
import coisas from "./components/coisas.vue";
export default {
    name: "App",
    components: {
        novo,
        coisas
    },
    data() {
        return {
            tarefa: [
                {
                    item: "estudar"
                }
            ]
        };
    },
    methods: {
        adicionar: function(event) {
            this.tarefa.push({
                item: event.item
           });
        }
    }
};
</script>

<style>
</style>