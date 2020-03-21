<template>

  <div class="home">

    <span> beers : {{ this.beers }} </span>

    <p>
      <input v-model="id" :text="1" type="number">
    </p>

    <p>

      <input v-model="nom" placeholder="nom">
    </p>
    <p>
      <input v-model="comment" placeholder="comment">
    </p>
    <p>
      <input v-model="priceHT" placeholder="priceHT">
    </p>
    <p>
      <input v-model="priceTTC" placeholder="priceTTC">
    </p>
    <p>
      <input v-model="alcool" placeholder="alcool">
    </p>
    <p>
      <input v-model="type" placeholder="type">
    </p>
    <p>
      <input v-model="owner" placeholder="owner">
    </p>

    <p>
      <button v-on:click="addBeer">Add</button>
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
      id: 0,
      nom: '',
      comment: '',
      priceHT: null,
      priceTTC: null,
      alcool: '',
      type: '',
      owner: ''
    }
  },
  methods: {
    addBeer() {
      const beer = {
        id: this.id,
        nom: this.nom,
        comment: this.comment,
        priceHT: this.priceHT,
        priceTTC: this.priceTTC,
        alcool: this.alcool,
        type: this.type,
        owner: this.owner
      }
      this.beers.push(beer)
      console.log(this.beers)
      this.beer.id += 1
    }
  },
  created: function() {
    this.id = 0
  }
}
</script>
