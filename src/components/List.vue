<template>
  <div class="container">

        <router-link to="/detail">Detail</router-link>

        <div  v-for="e in elements" v-bind:key="e.id">
            <router-link :to=" '/detail/' + e.id">
                <b-card
                    :title="e.title"
                >

                <b-card-text>
                    {{ e.description }}
                </b-card-text>

                </b-card>
            </router-link>
        </div>

  </div>
</template>

<script>
export default {

    created(){
        this.findAll()
    },
    data(){
        return {
            elements: []
        };
    },
    methods: {
        findAll: function(){
            fetch('http://localhost:8000/api/element/?format=json')
            .then(res => res.json())
            .then(res => this.elements = res)
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