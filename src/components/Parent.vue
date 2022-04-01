<template>
    <div>
    <!--   <Child Name = "Sai" />      
        <table align="center">
      <thead>
        <tr>
          <td>Name</td>
          <td>PhoneNo</td>
        </tr>
      </thead>
      <tbody>
        <td>{{Name}}</td>
        <td>{{PhoneNo}}</td>
      </tbody>
    </table> -->
        </div>
</template>

<script>
//import Child from './Child.vue'

export default {
    name :"ParenT",
    data() {
        return{
            Name:"Sai Prashanth",
            PhoneNo:"87236473"
        }
        
    },
    components:{
     //   Child,
    },
    methods:{ result(){
        this.Name = this.data.Name
        this.PhoneNo = this.data.PhoneNo
    }

    }
}
</script>
