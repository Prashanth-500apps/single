<template>
    <div>
        <Parent />
  <!--  <h1>Name:{{ Name }}</h1>
    <h1>PhoneNo: {{ PhoneNo }}</h1> -->
    <form><label>Name:</label><input
      type="text"
      placeholder="enter the text"
      @change="$emit('Name', $event.target.value)"
    /><br><br>
   <label>Number:</label> <input
    type="integer"
    placeholder="Enter Number"
    @change="$emit('PhoneNo',$event.target.value)"/></form><br>

    <button type="submit" @click = result() >Submit</button>
    </div>
</template>

<script>
import Parent from './Parent.vue'

export default {
    name:"ChiLD",
    emit:{
        Name:String,
        PhoneNo:Number,
    },
    data() {
     
    },
    components:{
        Parent,
    },
    methods: {
    Name(event) {
      this.$emit("saiprashanth", event.target.value);
    },
    PhoneNo(event) {
        this.$emit("763597398", event.target.value);
    },
    result(){
          
    }
   
},
}
</script>
