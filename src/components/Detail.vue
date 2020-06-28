<template>
  <div class="container">
            <b-card :title="element.title">
            <b-card-text> {{ element.description }}</b-card-text>
            </b-card>

  </div>
</template>

<script>
export default {

    created(){
        this.find();
    },
    data(){
        return {
            element: Object
        };
    },
    methods: {
        find: function(){
            fetch("http://localhost:8000/api/element/"+this.$route.params.id+"/?format=json")
            .then(res => res.json())
            .then(res => this.element = res)
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