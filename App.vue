<script>
import { loginUrl } from './config.js'
export default {
  data () {
    return {
      login: {
        email: 'sai.vichet70@gmail.com',
        password: 'kaka'
      }
    }
  },
  methods: {
    handleLoginFormSubmit () {
      const postData = {
        grant_type: 'password',
        client_id: '',
        client_secret: '',
        username: 'sai.vichet70@gmail.com',
        password: 'kaka',
        scope: ''
      }
      this.$http.post(loginUrl, postData)
    }
  }
}
</script>
<template>
  <div class="wrapper" id="home-wrapper">
    <section class = "login">
      <div class="row">
        <div class="col-md-6 col-md-push-3">
          <div class="panel panel-default">
            <div class="panel-heading">
              <strong>Login</strong>
            </div>
            <div class="panel-body">
              <form  v-on:submit.prevent="handleLoginFormSubmit()">
                <div class="form-group">
                  <label>Email address</label>
                  <input class="form-control" placeholder="Enter your email address" type="text" v-model="login.email">
                </div>
                <div class="form-group">
                  <label>Password</label>
                  <input type="password" class="form-control" placeholder="Enter your password" v-model="login.password">
                </div>
                <button class="btn btn-primary">Login</button>
              </form>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="sass">
  @import './assets/css/bootstrap.css'
</style>
