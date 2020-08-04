<template>
  <div class="hello">
    <Picture
      imgName="corcora_valley.jpg"
      altText="workbench"
    />
  </div>
</template>

<script>
import Picture from './Picture'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    Picture
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
}
</style>
