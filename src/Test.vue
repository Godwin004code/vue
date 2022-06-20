

<template>
  
   <div>
     <h2>{{title}}</h2>
  <input type="text" ref="name" />
  <button @click="handleClick">Click me</button>
  <Modal :header='header :text="text" />
   </div>
</template>
// https://github.com/LordRahl90/realdot-admin.git
<script>
import Modal from "./components/Modal.vue"

export default {


  components: {
    Modal
  },
  data: function() {
      return {
        title :  'Hello Vue from Godwin',
      header : 'modal head',
      text : 'Giveaway time'
      };
      
    
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name);
      this.$refs.name.classList.add('active')
   
      this.$refs.name.focus()
    }
  }
}
</script>




// template refs can be see as a way to draw element from the DOM,like the way we usequeryselector or getbyid in vanilla. You add a ref attribute to an element, then you draw ///it using this.$ref.the name of the ref