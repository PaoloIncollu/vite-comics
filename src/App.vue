<script>
/* 
  Per importare ed utilizzare un componente dentro un altro devo SEMPRE seguire questi 3 passi:
  1) Importazione del componente
  2) Dichiarazione del componente
  3) Utilizzo del componente
*/
// 1) Importazione del componente
import AppHeader from './components/AppHeader.vue';

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

      listInfo:[
        {
          label:'DIGITAL COMICS',
          img:'../public/img/buy-comics-digital-comics.png'
        },
        {
          label:'DC MERCHANDISE',
          img:'../public/img/buy-comics-merchandise.png'
        },
        {
          label:'SUBSCRIPTION',
          img:'../public/img/buy-comics-subscriptions.png'
        },
        {
          label:'COMIC SHOP LOCATOR',
          img:'../public/img/buy-comics-shop-locator.png'
        },
        {
          label:'DC POWER VISA',
          img:'../public/img/buy-dc-power-visa.svg'
        }
      ]
      
      
    }
  },
  // 2) Dichiarazione del componente
  components: {
    AppHeader
  },
  methods: {
    
  }
}
</script>

<template>
  <div class="my-container">
    <!-- 3) Utilizzo del componente -->
    <header>
      <div>
        <div>
          <img src="../public/img/dc-logo.png" alt="DC logo">
        </div>
        
        <ul>
          <li v-for="(nav,index) in navBar" >
            {{ nav.label }}
          </li>
        </ul>
      </div>
    </header>
    
    <main>
      <div>
        <h3>

          --&gt; Content goes here &lt;--

        </h3>
      </div>
      
    </main>

    <footer>
      <div class="footer-top">
        <ul>
          <li v-for="(item,index) in listInfo">

            <div>
              <img :src="item.img" :alt="item.label">
            </div>
            
            <span>
              {{ item.label }}
            </span>
          </li>
        </ul>

      </div>

      <div class="footer-bottom">

      </div>
    </footer>
  </div>
</template>

<style lang="scss" scoped>
header{
  div{

    width: 80%;
    padding: 10px 0;
    margin: 0 auto;
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

      list-style: none;
      display: flex;

      
      li{

        padding: 20px;
        font-weight: bold;
        color: #647682;

      }
    }
    
  }
}

main{

  background-color: black;

  div{

    width: 80%;
    margin: 0 auto;
    color: white;
    padding: 50px 0;
  }
  
}

footer{
  div{

    background-color: #0282F9;

    ul{

      width: 80%;
      margin: 0 auto;
      padding: 40px;
      display: flex;
      justify-content: space-around;

      li{
        display: flex;
        list-style: none;
        color: white;
        
        div{

          width: 80px;
          
          align-self: center;
          
        }
        span{

          padding: 0 25px;
          align-self: center;
        }
      }
    }
  }
}
</style>
