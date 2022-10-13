<template>
  <div>
    <h1>메인페이지</h1>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  async created() {
    try {
      const response = await axios.get('http://localhost:3000/products')
      console.log('에러없다', response)
    } catch (error) {
      console.log(error)
    }
  },
}
</script>
<style scoped></style>
