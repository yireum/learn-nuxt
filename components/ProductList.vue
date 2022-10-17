<template>
  <div>{{ products }}</div>
</template>
<script>
import axios from 'axios'
export default {
  async asyncData() {
    const response = await axios.get('http://localhost:3000/products')
    console.log(response)
    const products = response.data
    return { products }
  },
}
</script>
<style scoped></style>
