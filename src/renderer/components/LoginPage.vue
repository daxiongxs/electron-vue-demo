<template>
  <div class="wrapper">
    <main>
      <el-input v-model="user" placeholder="用户名"></el-input>
      <el-input v-model="password" placeholder="密码"></el-input>
    </main>
  </div>
</template>

<script>
  import SystemInformation from './LandingPage/SystemInformation'

  export default {
    name: 'login-page',
    components: { SystemInformation },
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body { font-family: 'Source Sans Pro', sans-serif; }
  el-input {color: aquamarine}
  .wrapper {
    background: url('~@/assets/login-bg.png');
    background-size: contain;
    background-repeat: no-repeat;
    height: 462px;
    width: 1186px;
  }

  main {
    display: flex;
    justify-content: space-between;
  }

  main > div { flex-basis: 50%; }

  .user {
    display: flex;
    left: 1000px;
    top: 100px;
    width: 80px;
    height: 20px;
  }

  .password {
    display: flex;
    left: 1000px;
    top: 100px;
    width: 80px;
    height: 20px;
  }
</style>
