<template>
  <div class="hello">
    <input type="text" v-model="msg">
    <MyComponent :msg="msg" :myFunc="testAlert" :myFunct="test" />
            <vue-progress-bar></vue-progress-bar>
            <button @click="AlertToggle">Click</button>
 
    <carousel-3d>
	    <slide :index="0">
	      <img src="https://img.staticbg.com/images/oaupload/banggood/images/4C/DA/5498416b-1e0c-4cff-a7fe-164f3d2d8b80.jpg">
	    </slide>
	    <slide :index="1">
	      Slide 2 Content
	    </slide>
      <slide :index="2">
	      Slide 2 Content
	    </slide>
	  </carousel-3d>
   </div>
</template>

<script>
import MyComponent from './MyComponents'
import { Carousel3d, Slide } from 'vue-carousel-3d'
export default {
  name: 'HelloWorld',
  components: {
    MyComponent: MyComponent,
    Carousel3d,
    Slide
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    testAlert(msg) {
      alert("test" + msg)
    },
    test(){
      console.log("hi")
    },
    AlertToggle () {
			this.$swal('Hello Vue world!!!')
		}
  },
 created () {
    this.$Progress.start()
  },
  mounted () {
    this.$Progress.finish()
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
