<template>
  <div class="top-menu">
      <ul>
        <li v-for="item in items">
          <router-link :to="item.route">{{ item.name }}</router-link>
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'top-menu',
  data() {
    return {
      items: [
        {
          route: '/',
          name: 'Home',
        },
        {
          route: '/about',
          name: 'About',
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
}
</style>
