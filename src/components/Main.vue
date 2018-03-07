<template>
  <div>
    <Navbar v-for="(navbar, i) in navbars" :key="i" :color="navbar.color" :config="navbar.config" :items="navbar.items"></Navbar>
    <div v-bind:class="{ 'container-fluid': fluid }">

    </div>
  </div>
</template>

<script>
import Navbar from './Navbar'

export default {
  name: 'Main',
  data () {
    return {
      fluid: true,
      columns: [
        {
          type: 'sm',
          size: 6
        }
      ],
      navbars: [{
        items: [{
          name: 'Active',
          href: '#',
          active: true
        }, {
          name: 'Disabled',
          href: '#'
        }, {
          name: 'About Us',
          href: '#'
        }],
        color: 'blue',
        config: {
          title: 'Personalize o Menu',
          content: '<button class="btn btn-primary">Adicionar Item</button>',
          placement: 'bottom',
          target: 'popoverButton-open'
        }
      }]
    }
  },
  methods () {
    return {
    }
  },
  components: {
    Navbar
  }
}
</script>

<style scoped>
</style>
