<template>
  <div class="home">
    이곳은 {{$route.params.id}} 게시판입니다.<br>
    {{$route.query.q}}
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Board',
  // data(){
  //   return{
  //     boardName: ""
  //   }
  // },
  // created() {
  //   this.boardName = this.$route.params.id
  // },
  components: {
    
  }
}
</script>
