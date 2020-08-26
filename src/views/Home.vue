<template>
  <div class="home">
    <main>
      <h1> Hey {{user.name}} you have been authenticated </h1>
      <div>
        <h4> These are your details... </h4>
        <p> Email: {{user.email}}</p>
        <p> Full Name: {{user.name}}</p>
      </div>
    </main>
  </div>
</template>

<script>
// @ is an alias to /src
import { mapGetters } from 'vuex'
export default {
  name: 'Home',
  components: {

  },
  computed: {
    ...mapGetters(['user'])
  }
}
</script>

<style scoped>
  main{
    padding: 2rem;
    display: grid;
    place-content: center;
  }

  h1{
    font-size: 36px;
  }
</style>
