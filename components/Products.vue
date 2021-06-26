<template>
<div class="row p-md-5 p-xs-2">
      <div class="col-md-3 mb-4" v-for="product of products" :key="product.id">
          <div class="card">
      <img :src="product.image" alt="" class="card-img-top card-image-wrapp">
      <div class="card-body">
        <h5 class="card-title">{{product.title}}</h5>
        <h6 class="card-subtitle mb-2 text-muted">{{product.category}}</h6>
        <p class="card-text">Lorem ipsum dolor aborum, rerum voluptates ipsam eos quo tempore iusto dolore modi dolorum in pariatur. Incidunt repellendus praesentium quae!</p>
       <button class="btn btn-outline-success btn-sm">Buy {{product.price}} $</button>
        <button class="btn btn-outline-primary btn-sm">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-cart" viewBox="0 0 16 16">
  <path d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .491.592l-1.5 8A.5.5 0 0 1 13 12H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5zM3.102 4l1.313 7h8.17l1.313-7H3.102zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm-7 1a1 1 0 1 1 0 2 1 1 0 0 1 0-2zm7 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"/>
</svg>
        </button>
      </div>
      </div>
      </div>
</div>
</template>

<script>
import dayjs from 'dayjs'

  export default {
    data() {
      return {
        products: [],
        todaysDate : dayjs().format('DD-MM-YYYY')
      }
    },
    async fetch() {
      this.products = await fetch(
        'https://fakestoreapi.com/products'
      ).then(res => res.json())
    }
  }
</script>

<style>
.card-image-wrapp{
    height: 200px;
    object-fit: cover;
}
</style>

