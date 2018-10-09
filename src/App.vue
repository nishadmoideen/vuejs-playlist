<template>
  <div>
    <!--
    <h1>{{ title }}</h1>
    <ninjas></ninjas>
    //-->
    <app-header v-bind:title="title" v-on:titleChanged='updateTitle($event)'></app-header>
    <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>
    <hr/>
     <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Ninjas from './components/Ninjas.vue';

export default {
  components: {
    'app-header': Header,
    'app-footer': Footer,
    'app-ninjas': Ninjas
  },
  data () {
    return {
      title: 'View Ninjas',
      ninjas: [
          {name: 'Yoshi', speciality:'Vue Components', show: false},
          {name: 'Mario', speciality:'HTML Wizardry', show: false},
          {name: 'Hitoshi', speciality:'Click Components', show: false},
          {name: 'Kami', speciality:'Webpack', show: false},
          {name: 'Tango', speciality:'Data Design', show: false},
          ]
    }
  },
  methods: {
    updateTitle: function(newTitle) {
      this.title=newTitle;
    }
  }
}
</script>

<style>
h1 {
    color: purple;
}

</style>
