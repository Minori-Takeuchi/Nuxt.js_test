<template>
  <div class="container">
    <div>
      <h2>生徒一覧</h2>
      <nuxt-link to="/students">生徒の情報を見る</nuxt-link>
    </div>
    <div>
      <h2>管理者</h2>
      <nuxt-link to="/management">管理画面を見る</nuxt-link>
    </div>
  </div>
</template>

<style>
.container {
  margin: 0 auto;
  width: 500px;
  min-height: 100vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
}
</style>