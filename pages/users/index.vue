<template>
  <div>
    <input v-model="userId" type="text"/>
    <button @click="onLoadUser">submit</button>
    <p>Please Enter user id</p>
    <nuxt-child/>
    
  </div>
</template>
<script>
export default{
    data(){
        return {
            userId: ''
        }
    },
    methods: {
        onLoadUser(){
            this.$router.push('/users/' + this.userId)
        }
    }

} 
</script>

