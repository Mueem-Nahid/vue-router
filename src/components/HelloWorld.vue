<template>
  <div class="hello">
    <h2>This is home</h2>
    <div>
      <h5>All Users:</h5>
      <ul>
        <li v-for="(user, index) in users" :key="index">
          <router-link :to="{ name:'Profile', params: {user: user} }"> User name {{user}} </router-link>
        </li>
      </ul>
    </div>
    <!-- details -->
    <div>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      users: [
        'Akash', 'Abir', 'Hasnat', 'Riad', 'Eshti'
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
  text-decoration: none;
}
</style>
