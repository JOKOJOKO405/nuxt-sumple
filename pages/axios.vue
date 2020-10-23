<template>
  <div>
    <p>{{ ip }}</p>
    <button @click="getIp">IPアドレス取得</button>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      ip: '127.0.0.1',
    }
  },
  methods: {
    async getIp(){
      this.ip = await this.$axios.$get('http://icanhazip.com')
    }
  }
}
</script>