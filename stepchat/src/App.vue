<template>
  <div id="app">
    <Header />
    <Content />
    <MessageForm />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Content from './components/Content.vue'
import MessageForm from './components/MessageForm.vue'

export default {
  name: 'App',
  components: {
    Header,
    Content,
    MessageForm
  },
  data: function () {
    return {
      root: 'http://localhost:3000', // TODO: http://api.stepchat.site
      users: 'http://localhost:3000/user',
      messages: 'http://localhost:3000/message',
      messagesList: null,
      userlist: null
    }
  },
  async beforeMount () {
    setInterval(async () => {
      const response = await fetch(this.root)
      if (response.ok) {
        const data = await response.json()
        this.messagesList = data.messages
        this.usersList = data.users
      }
    }, 1000)
  }
}
</script>

<style lang="scss">
body {
  margin: 0px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
