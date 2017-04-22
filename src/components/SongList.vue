<template>
  <div class="hello">
    <h3>SongList</h3>
    <ul class="collection">
      <li class="collection-item" v-for="song in songs">{{song.title}}</li>
    </ul>
  </div>
</template>

<script>
import gql from 'graphql-tag'

export default {
  name: 'hello',
  apollo: {
    songs: gql`{ songs { id, title } }`
  },
  data () {
    return {
      songs: ['Loading...']
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
