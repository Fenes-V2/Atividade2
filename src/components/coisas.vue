<template>
    <div id="tarefasio">
        <div class="trabalhos" v-for="(afazer, index) in tarefa" :key="index">
        {{ afazer.item }} <input type="checkbox" name="" id="">
        </div>
    </div>
</template>

<script>
export default {
    name: "coisas",
    props: ["tarefa"]
};
</script>

<style>
#tarefasio {
    width: 380px;
    height: 300px;
    border: 3px solid #ffffff;
    margin: 1px auto 0 auto;
    padding: 10px;
}
</style>