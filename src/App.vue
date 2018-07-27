<template>
  <div id="app">
    <header>
      <span>News Feeds</span>
    </header>
   <SourceSelection v-on:sourceChanged="sourceChanged"></SourceSelection>
    <Newslist v-bind:source="source"></Newslist>
    
    <div class="footer">
    </div>
  </div>
</template>


<script>
import Newslist from './components/Newslist'
import SourceSelection from './components/SourceSelection'
export default {
  name: 'app',
  components: {
    Newslist,
    SourceSelection
  },
  data () {
    return {
      source: ""
    }
  },
  methods: {
    sourceChanged: function (source) {
      this.source = source;
    }
  }
}
</script>

<style>

  header {
  margin: 0;
  height: 56px;
  padding: 0 16px 0 24px;
  background-color: #35495E;
  color: #ffffff;
}

header span {
  display: block;
  position: relative;
  font-size: 20px;
  line-height: 1;
  letter-spacing: .02em;
  font-weight: 400;
  box-sizing: border-box;
  padding-top: 16px;
}
</style>