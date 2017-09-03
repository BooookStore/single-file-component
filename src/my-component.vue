<template>
  <p class="message">
    メッセージ : {{ message }}
  </p>
</template>

<style>
.message {
  color: #42b983;
}
</style>

<script>
module.exports = {
  data: function () {
    return {
      message: 'A'
    }
  }
}
</script>
