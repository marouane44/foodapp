<template>
  <main class="container restaurant">
    
  
    <div class="restaurantheading">
      <h1>Restaurants</h1>
      <AppSelect @change="selectedRestaurant = $event"/>
      <pre>{{$data}}</pre>
    </div>

    <AppRestaurantInfo />
  </main>
</template>

<script>
import AppRestaurantInfo from "@/components/AppRestaurantInfo.vue";
import AppSelect from '@/components/AppSelect.vue';
export default {
  components: {
    AppSelect,
    AppRestaurantInfo
  },
  data(){
    return {
      selectedRestaurant: "",
    };
  }
};
</script>

<style lang="scss" scoped></style>
