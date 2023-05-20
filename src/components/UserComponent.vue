<template>
  {{name}}
</template>

<script>
import {computed, reactive, toRefs} from "vue";
export default {
  name: "UserComponent",
  setup(){
    const userInfo = reactive({
      firstname: "Mahmoud",
      lastname: "Magdy",
      fullname: computed(()=>{
        return userInfo.firstname + " " + userInfo.lastname;
      })
    });

    function change(){}

    return {...toRefs(userInfo) , change};
  }
}

</script>

<style scoped>

</style>