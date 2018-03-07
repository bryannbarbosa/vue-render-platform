<template>
  <nav v-b-popover.hover.html="config" variant="success" class="navbar navbar-expand-sm bg-dark navbar-dark" v-bind:class="[color, textcolor]">
    <ul class="navbar-nav">
      <li v-for="(item, i) in items" :key="i" class="nav-item">
        <a class="nav-link" v-bind:class="{ 'active': item.active }" v-bind:href="item.href">{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  props: ['items', 'color', 'textcolor', 'config'],
  data () {
    return {
    }
  }
}
</script>

<style scoped>
.red {
  background-color: red !important;
}
.green {
  background-color: green !important;
}

.black {
  background-color: black !important;
}

</style>
