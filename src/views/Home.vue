<template>
  <div class="home">
    <input type="text" @change="getText" />
    <button type="submit" @click="reversText">Press</button>
  </div>
</template>

<script>
export default {
  name: "Home",
  data(){
    return{
      input_text: ""
    }
  },
  methods:{
    getText(e){
      this.input_text=e.target.value
    console.log(this.input_text.split(" "),"input_text")
    },
    reversText(){
      const textArray= this.input_text.split(" ")
      console.log(textArray,'textArray');
      // for(let i=0;i<textArray.length;i++){
      //   textArray[i]=textArray[i].split("").reverse().join("")
      //   console.log(textArray[i],"loop")
      // }
      console.log(textArray.reverse().join(" "),"final");

    }
  }
};
</script>
