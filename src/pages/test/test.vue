<template>
    <div>
        <button class="test" v-bind:style="{backgroundColor:backgroundColor ? 'red':'yellow'}" @click="changecolor">{{ test }}</button>
        <input type="text" v-bind:value="test" v-on:input="test1($event)">
    </div>
</template>

<script>
export default {
  data () {
    return {
      test: 1,
      backgroundColor:true
    }
  },
  methods:{
    test1:function(e){
     this.test=e.target.value;
    },
    changecolor:function () {
      this.backgroundColor=!this.backgroundColor;
    }
  },
  computed:{
  }

}
</script>
