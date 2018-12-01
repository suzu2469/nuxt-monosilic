<template>
  <section class="container">
    <ul>
      <li
        v-for="(product, key) in products"
        :key="key"
      >{{ product.name }}: {{ product.price }}</li>
    </ul>
  </section>
</template>

<script>
export default {
  asyncData({ res }) {
    return {
      products: res.context.products
    }
  }
}
</script>
