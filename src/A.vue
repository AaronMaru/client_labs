<!-- <template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>

import HelloWorld from '@/components/HelloWorld'

export default {
  components: {
    HelloWorld
  },

  created () {
    const postData = {
      grant_type: 'password',
      client_id: 2,
      client_secret: 'xpQAk9YkS3jtdT9H5RFJYaWANninZpMsPS7jI4aI',
      username: 'sai.vichet70@gmail.com',
      password: 'kaka',
      scope: ''
    }
    this.$http.post('http://localhost:8000/oauth/token', postData).then(
      response => {
        console.log('dd : ', response)
        const header = {
          'Accept': 'application/json',
          'Authorization': 'Bearer ' + response.body.access_token
        }
        this.$http.get('http://localhost:8000/api/user', { headers: header }).then(
          response => {
            console.log('dd : ', response)
          }
        )
      }
    )
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style> -->
