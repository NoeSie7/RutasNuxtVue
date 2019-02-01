<template>
  <div class="container">
    <div>
      <span><h3>Ha cambiado tu valor en la ruta :  {{val}}</h3></span>
    </div>
  </div>
</template>
<script>
export default {
  validate({params}){
    console.log(params);
    return /^\d+$/.test(params.id)
  },
  data() {
    return {
      val: this.$route.params.id
    }
  },
  layout: 'header'
}
</script>
