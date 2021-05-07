<template>
  <div>
    <nav class="navbar navbar-light bg-light">
      <a class="navbar-brand" href="#">
        <font-awesome-icon :icon="['fab', 'youtube']" style="color:red;" class="mr-1" /> <span class="logo">Youtube</span>
      </a>
      <div class="d-flex justify-content-center ml-auto user-content">
        <div class="search d-flex align-items-center">
          <font-awesome-icon :icon="['fas', 'search']" style="font-size: 20px;"/>
        </div>
        <div class="user ml-3 d-flex justify-content-center align-items-center">R</div>
      </div>
      <div class="badge-content w-100">
        <ul class="list-group flex-row w-100 rounded-0 border-top border-dark">
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">All</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">Music</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">One Direction</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">History</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">王力宏</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">30 Seconds</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">G.E.M</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">灌籃高手</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">Energy</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">外國人來台灣</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">10大精選</span>
          </li>
          <li class="list-group-item border-0">
            <span class="badge badge-secondary text-light bg-secondary">惡靈古堡</span>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
import $ from 'jquery'
export default {
  name: 'Navbar',
  data () {
    return {
      lastPageHeight: 0
    }
  },
  methods: {
    navbarscroll () {
      window.addEventListener('scroll', function () {
        let scrollDir = window.scrollY > 10 ? 1 : 0
        if (scrollDir) {
          $('.navbar').addClass('navscroll')
        } else {
          $('.navbar').removeClass('navscroll')
        }
      })
    }
  },
  created () {
    this.navbarscroll()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.navbar-brand {
  margin-left: 5px;
}
.user-content {
  margin-right: 5px;
}
.logo {
  font-weight: 600;
}
.search {
  margin-right: 30px;
}
.user {
  border-radius: 50%;
  width: 30px;
  height: 30px;
  background-color: green;
  color: white;
}
.badge {
  font-size: 20px;
  border-radius: 20px;
  padding: 10px;
}
.list-group {
  overflow-x: auto;
}
.navscroll {
  box-shadow: 5px 5px rgba(0, 0, 0, 0.4);
}
</style>
