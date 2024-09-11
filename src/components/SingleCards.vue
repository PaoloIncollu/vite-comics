<script>

export default {

  props:{

    card:Object

  }

}

</script>

<template>

  <div class="my-card" >
    
    <img :src="card.thumb" :alt="card.series">

    <div class="my-card-body">

      <h4>

        {{ card.series}}

      </h4>
  
    </div>

  </div>

</template>

<style lang="scss" scoped>

@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;

.my-card{
  
  width: calc(100% / 6);
  padding:20px 10px;
          
  img{

  width: 250px;
  height: 250px;
  object-position: top;
        
  }

  h4{

    padding-top: 10px;
    color: $my-color-link;

  }
}

</style>