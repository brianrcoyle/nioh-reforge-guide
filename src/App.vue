<template>
  <div id="app">
    <div id="router">
      <router-view></router-view>
    </div>
    <div id="links">
      <h1>{{ CONSTANTS.INDEX_HEADER }}</h1>
      <ul>
        <li>
          <router-link to="/armor">{{ CONSTANTS.ARMOR_LINK }}</router-link>
        </li>
        <li>
          <router-link to="/melee">{{ CONSTANTS.MELEE_LINK }}</router-link>
        </li>
        <li>
          <router-link to="/ranged">{{ CONSTANTS.RANGED_LINK }}</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  import CONSTANTS from './data/app-data';

  export default {
    name: 'app',
    data() {
      return {
        CONSTANTS,
      };
    },
  };
</script>

<style>
  #app {
    margin-left: 20px;
  }

  h1, h2 {
    font-weight: normal;
    font-style: italic;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    margin: 10px 0;
  }

  a {
    color: #42b983;
  }

  img {
    max-width: 100%;
  }

  a:hover {
    color: #2b6b53;
    text-decoration: none;
  }
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }
  #router {
    width: 49%;
    float: left;
  }
  #links {
    text-align: center;
  }
</style>
