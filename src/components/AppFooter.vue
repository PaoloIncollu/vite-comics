<script>
export default {
  data() {
    return { 
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
      ],

      linkUtili:[
        {
          title:'DC COMICS',
          options:[
            {
              option:'Character'
            },
            {
              option:'Comics'
            },
            {
              option:'Movies'
            },
            {
              option:'TV'
            },
            {
              option:'Games'
            },
            {
              option:'Videos'
            },
            {
              option:'News'
            }


          ]
        },
        {
          title:'SHOP',
          options:[
            {
              option:'Shop DC'
            },
            {
              option:'Shop DC Collectibles'
            }


          ]
        },
        {
          title:'DC',
          options:[
            {
              option:'Therms Of Use'
            },
            {
              option:'Privacy policy (New)'
            },
            {
              option:'Ad Choices'
            },
            {
              option:'Advertising'
            },
            {
              option:'Jobs'
            },
            {
              option:'Subscriptions'
            },
            {
              option:'Talent Workshops'
            },
            {
              option:'CPSC Certicates'
            },
            {
              option:'Ratings'
            },
            {
              option:'Shop Help'
            },
            {
              option:'Contact Us'
            }


          ]
        },
        {
          title:'SITES',
          options:[
            {
              option:'DC'
            },
            {
              option:'MAD Magazine'
            },
            {
              option:'DC Kids'
            },
            {
              option:'DC Universe'
            },
            {
              option:'DC Power Visa'
            }
            


          ]
        },

        
      ],

      listSocial:[
        {
          title:'FOLLOW US',
          social:[
            {
              name:'Facebook',
              icon:'../../public/img/footer-facebook.png'
            },
            {
              name:'Twitter',
              icon:'../../public/img/footer-twitter.png'
            },
            {
              name:'Youtube',
              icon:'../../public/img/footer-youtube.png'
            },
            {
              name:'Pinterest',
              icon:'../../public/img/footer-pinterest.png'
            },
            {
              name:'Perinpnscope',
              icon:'../../public/img/footer-periscope.png'
            }
          ]
        }
      ]
}
  }}
</script>

<template>
    <footer>
      <div class="container-footer">
        <div class="footer-top">
          <ul>
            <li v-for="(item,index) in listInfo" :key="index">

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
        

          <div class="footer-bottom-top">

            <div class="container-link-utili">
              <ul v-for="(comics,index) in linkUtili" :key="index">

                <h4>
                  {{ comics.title }}
                </h4>

                <li v-for="(opt,index) in linkUtili[index].options" :key="index">

                  {{opt.option }}

                </li>

              </ul><div class="logo-footer">

          <img src="../../public/img/dc-logo-bg.png" alt="">
              
            </div>
            </div>
            
            
          </div>
          
        
          <div class="container-bg-grey-footer">

            <div class="footer-bottom-bottom">

              <div>

                <button>SIGN-UP NOW!</button>

              </div>

              <div class="icons-social">
                <ul v-for="(social,index) in listSocial" :key="index">

                  <h4>
                    {{ social.title }}
                  </h4>

                  <li v-for="(iconSocial,index) in listSocial[index].social" :key="index">

                    <a href="#">

                      <img :src="iconSocial.icon" :alt="iconSocial.icon">

                    </a>

                  </li>

                </ul>
              </div>
            </div>
          </div>
          
      </div>  
    </div>
        
      
    </footer>
</template>

<style lang="scss" scoped>

footer{
  width: 100%;
  position: absolute;
  bottom: 0;
  left: 0; 
  background-image: url('../public/img/footer-bg.jpg');
  background-size: cover;
  
  .container-footer{
    
    position: relative;
    z-index: 1;
    width: 100%;
    
    

    .footer-top{
      
      background-color: #0282F9;
      width: 100%;
      
      ul{

        width: 80%;
        margin: 0 auto;
        padding: 40px;
        display: flex;
        justify-content: space-between;
        

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

    .footer-bottom-top{

      width: 80%;
      height: 350px;
      margin: 30px auto;
      
      .logo-footer{
        z-index: 2;
        position: absolute;
        top: 150px;
        right: 200px;
        width: 500px;
        height: 500px;
      }

      .container-link-utili{
        
        width: 30%;
        height: 100%;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        
        ul{

          list-style: none;
          padding-bottom: 10px;
                    
          h4{
            color: white;
            font-weight: bold;
            padding-bottom: 10px;
          }
                    
          li{
            color: grey;
            
          }
        }
      }
    } 

    .container-bg-grey-footer{
      position: fixed;
      bottom: 0;
      left: 0;
      z-index: 2;
      width: 100%;
      height: 100px;
      background-color:#303030;
      

      .footer-bottom-bottom{
        
        width: 80%;
        height: 100px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        
      div{
        button{

          padding: 10px 8px;
          border: 2px solid #0282F9;
          background-color: #303030;
          color: white;
          font-weight: bold;
        }
      }
      

      .icons-social{

        ul{

          display: flex;
          align-items: center;
          list-style: none;
          
          h4{

            color: #0282F9;
            padding-left: 10px;
          }

          li{

            a{

              display: block;
              width: 50px;
              padding: 0 10px;
            }
          }
        }

      }
      
    }
    }
    
  }
  
}

</style>
