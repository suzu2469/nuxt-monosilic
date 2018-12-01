<template>
  <section class="container">
    <ul>
      <li
        v-for="(product, key) in products"
        :key="key"
      >{{ product.name }}: {{ product.price }}</li>
    </ul>
    <!-- クライアントスクリプトが実行されてるか確認用 -->
    <div>{{ getHello() }}</div>
  </section>
</template>

<script>
export default {
  asyncData({ res }) {
    return {
      products: res.context.products
    }
  },
  methods: {
    getHello() {
      return 'HelloWorld'
    }
  }
}
</script>
