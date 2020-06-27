<template>
  <div>
        <div class="box" v-for="e in elements" v-bind:key="e">
            {{ e }}
        </div>

        <button v-on:click="findAll">Click</button>

        {{ msj }}

  </div>
</template>

<script>
export default {
    data(){
        return {
            msj: ".... :(",
            elements: ["Uno", "Dos", "Tres"]
        };
    },
    methods: {
        findAll: function(){
            console.log("Hola Mundo")
            this.msj = "Click :)"
        }
    },
}
</script>

<style >
.box {
  border: 3px solid #ccc;
  margin: 5px 0 0 0;
}
</style>