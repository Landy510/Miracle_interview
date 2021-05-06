<template>
  <div>
    <footer>
      <div>
        <ul class="list-group flex-row justify-content-between">
          <li class="list-group-item border-0 text-center p-0 pt-1">
            <font-awesome-icon :icon="['fas', 'home']" style="font-size: 20px;"/>
            <p class="mb-0">Home</p>
          </li>
          <li class="list-group-item border-0 text-center p-0 pt-1">
            <font-awesome-icon :icon="['fas', 'fire']" style="font-size: 20px;"/>
            <p class="mb-0">Trending</p>
          </li>
          <li class="list-group-item border-0 text-center p-0 pt-1">
            <font-awesome-icon :icon="['fab', 'youtube-square']" style="font-size: 20px;"/>
            <p class="mb-0">Subscriptions</p>
          </li>
          <li class="list-group-item border-0 text-center p-0 pt-1">
            <font-awesome-icon :icon="['fas', 'book']" style="font-size: 20px;"/>
            <p class="mb-0">Library</p>
          </li>
        </ul>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.list-group-item {
   width:25%;
}
</style>
