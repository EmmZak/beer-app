<template>

  <div class="home">

    <span> beers : {{ this.beers }} </span>

    <p>
      <input v-model="this.beer.id" :text="1">
    </p>

    <p>

      <input v-model="this.beer.nom" placeholder="nom">
    </p>
    <p>
      <input v-model="this.beer.comment" placeholder="comment">
    </p>
    <p>
      <input v-model="this.beer.priceHT" placeholder="priceHT">
    </p>
    <p>
      <input v-model="this.beer.priceTTC" placeholder="priceTTC">
    </p>
    <p>
      <input v-model="this.beer.alcool" placeholder="alcool">
    </p>
    <p>
      <input v-model="this.beer.type" placeholder="type">
    </p>
    <p>
      <input v-model="this.beer.owner" placeholder="owner">
    </p>

    <p>
      <button v-on:click="add">Add</button>
    </p>
  </div>

</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',

  data: function() {
    return {
      beers: [],
      beer: {
        id: 0,
        nom: null,
        comment: null,
        priceHT: null,
        priceTTC: null,
        alcool: null,
        type: null,
        owner: null
      }
    }
  },
  methods: {
    add: function(e) {
      var b = { ...this.beer }
      this.beers.push(b)
      console.log(this.beers)
      this.beer.id += 1
    }
  },
  created: function() {
    this.beer.id = 0
  }
}
</script>
