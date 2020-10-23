<template>
  <div>
    <h2>ブログタイトル</h2>
    <p>これは{{ $route.params.id }}のエントリーです</p>
  </div>
</template>

<script>
export default {
  validate({ params }){
    return /^\d+$/.test(params.id);  // 数値かどうかの判定
  }
}
</script>