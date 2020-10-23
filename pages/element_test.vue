<template>
  <div>
    <h1>
      エレメント使用のテストページ
    </h1>
    <el-button @click="visible = true">エレメントボタン</el-button>
    <el-dialog :visible.sync="visible" title="確認">
      <p>処理されましたよ！</p>
    </el-dialog>
  </div>
</template>

<script>
export default {
  data: function(){
    return {
      visible: false,
    }
  }
}
</script>