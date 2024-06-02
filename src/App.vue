<template>
  <!-- <HeaderComponent></HeaderComponent> -->
  <router-view />
</template>

<script>
  import HeaderComponent from '@/components/HeaderComponent.vue';
  export default {
    components: {
      HeaderComponent
    }
  }
</script>

<style>
@import '../public/styles.scss';


input{
  border: 0;
  border-radius: 8px;
  width: 100%;
  height: 40px;
}

</style>
