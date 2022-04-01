<template>
    <div id = "Hello">
        <h1>Looping Items </h1>
        <p v-for = "user in arr" :key="user.id"></p>
        <p arr = {{arr}}></p>
        <p text = {{text}}> </p>
        <button @click="result(text)">OutPut</button>
        </div>
</template>

<script>

export default {
    name :"LooP",
    data(){
        return{
             arr : [{key:"mango",key:"orange",key:"banana",key:"34",key:"67",key:"apple"}],
             text = "",
        }
    },
    methods:{
            result(text) {
               this.text = this.arr.findIndex((text) => {
               return text;
      });
      console.log(this.text);
    },
},
}
</script>
