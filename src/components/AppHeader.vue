<script>
export default {
  data() {
    return { 
      navBar: [
        {
          label: 'CHARACTER',
          url: '#',
          active:false
                    
        },
        {
          label: 'COMICS',
          url: '#',
          active:true
                    
        },
        {
          label: 'MOVIES',
          url: '#',
          active:false
                    
        },
        {
          label: 'TV',
          url: '#',
          active:false
                    
        },
        {
          label: 'GAMES',
          url: '#',
          active:false
                    
        },
        {
          label: 'COLLECTIBLES',
          url: '#',
          active:false
                    
        },
        {
          label: 'VIDEOS',
          url: '#',
          active:false
                    
        },
        {
          label: 'FANS',
          url: '#',
          active:false
                    
        },
        {
          label: 'NEWS',
          url: '#',
          active:false
                    
        },
        {
          label: 'SHOP',
          url: '#',
          active:false
                    
        }
      
      ],
    }
  }
}
</script>

<template>
  <header>
      <div>
        <div>
          <img src="../../public/img/dc-logo.png" alt="DC logo">
        </div>
        
        <ul>
          <li v-for="(nav,index) in navBar" :key="index" >
            <a href="#">

              {{ nav.label }}

            </a>
            
          </li>
        </ul>
      </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;
header{

  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  height: 10vh;
  background-color: white;
  div{
    
    width: 80%;
    margin: 0 auto;
    height: 10vh;
    display: flex;
    justify-content: space-between;
    align-items: center;

    div{
      
      img{

        width: 80px;
        height: 80px;
      }

    }
    
    ul{

      @include list-ul;
      display: flex;

      
      li{

        padding: 20px;

        a{
         @include style-a;
         color: $my-color-link;
          &:hover{
            cursor: pointer;
            color: $my-blue;
            border-bottom:3px solid $my-blue;
          }
        }

      }
    }
    
  }
}
</style>
