
<template>
  <v-app>
    <component :is="currentLayout">
      <transition name="fade" mode="out-in">
        <router-view />
      </transition>
    </component>
  </v-app>
</template>
<script>
import index from "./views/Index.vue"
import admin from "./views/Admin.vue"
export default {
  components: {
    index,
    admin
  },
  data() {
    return {
      
    }
  },
  computed:{
    currentLayout(){
      const route = this.$route.meta.layout;
      return route;
    }
  },
  created(){
    console.log("route", this.$route.meta.layout);
  }
}
</script>


