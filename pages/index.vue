<template>
    <div class="h-screen w-screen">
        <div class="h-screen w-screen flex flex-col justify-center items-center" id="app">
          <div class = "main-text" @click="onDivClicked">
            <p class="text-4xl font-bold text-gray-800" unselectable="on"> {{ message }} </p>
            <br>
            <div class="font-bold text-emerald-700">WIP, will be completed later</div>
          </div>
            
        </div>
    </div>
    
</template>
<script>
  export default {
    data() {
      return {
        toggle: true,
        message: "Hello World"
      }
    },
    methods: {
      onDivClicked: function () {
        this.toggle = !this.toggle
        if (this.toggle){
          this.message = "Hello World"
        }
        else{
          this.message = "Goodbye World"
        }
      }
    }
  }
  </script>

