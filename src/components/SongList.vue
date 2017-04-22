<template>
  <div class="hello">
    <h3>SongList</h3>
    <ul>
      <li v-for="song in songs">{{song.title}}</li>
    </ul>
  </div>
</template>

<script>
import gql from 'graphql-tag'

export default {
  name: 'hello',
  apollo: {
    songs: gql`{ songs { title } }`
  },
  data () {
    return {
      songs: []
    }
  }
}
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
