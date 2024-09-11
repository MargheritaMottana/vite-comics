<script>

export default {

  data() {
    return {
      links:[
        {
          text : 'CHARACTERS',
          url : '#',
          active: false, 
        },
        {
          text : 'COMICS',
          url : '#',
          active: true,
        },
        {
          text : 'MOVIES',
          url : '#',
          active: false,
        },
        {
          text : 'TV',
          url : '#',
          active: false,
        },
        {
          text : 'GAMES',
          url : '#',
          active: false,
        },
        {
          text : 'COLLECTIBLES',
          url : '#',
          active: false,
        },
        {
          text : 'CHARACTERS',
          url : '#',
          active: false,
        },
        {
          text : 'VIDEOS',
          url : '#',
          active: false,
        },
        {
          text : 'FANS',
          url : '#',
          active: false,
        },
        {
          text : 'NEWS',
          url : '#',
          active: false,
        },
        {
          text : 'SHOP',
          url : '#',
          active: false,
        }
      ],
      products:[
        {
          text : 'DIGITAL COMICS',
          url : '#',
          image: '/public/img/buy-comics-digital-comics.png',
        },
        {
          text : 'DC MERCHANDISE',
          url : '#',
          image: '/public/img/buy-comics-merchandise.png',
        },
        {
          text : 'SUBSCRIPTION',
          url : '#',
          image: '/public/img/buy-comics-subscriptions.png',
        },
        {
          text : 'COMIC SHOP LOCATOR',
          url : '#',
          image: '/public/img/buy-comics-shop-locator.png',
        },
        {
          text : 'DC POWER VISA',
          url : '#',
          image: '/public/img/buy-dc-power-visa.svg',
        },
      ]
    }
  },

  methods:{

  },
}

</script>

<template>

  <header>

    <div class="container">

      <div class="flex">
            <!-- logo -->
            <img class="logo" src="/img/dc-logo.png" alt="DC">

            <!-- lista link -->
            <div>
                <ul>
                  <li v-for="(link, index) in links" :key="index">
                    <a :href="link.url" :class="link.active ? 'active' : '' " class="header-link"> {{ link.text }}</a>  
                  </li>
                </ul>
            </div>
      </div>

    </div>

  </header>

  <main>

    <!-- content -->
    <section class="bg-black">

      <div class="container">

        <section class="content flex">
            <div>
                --&gt Content goes here &lt--
            </div>
        </section>
        
      </div>

    </section>

    <!-- prodotti -->
    <section class="bg-blue">

      <div class="container">
          <section class="content flex">

            <ul>
              <li class="flex" v-for="(product, index) in products" :key="index">

                <a :href="product.url" class="flex product-container">

                  <img class="product-img" :src="product.image" :alt="product.text">
                  <span>
                    {{product.text}}
                  </span>

                </a>

              </li>
            </ul>

          </section>
      </div>

    </section>

  </main>

  <footer>

    <div class="container">

      <!-- footer top -->
      <section>

      </section>

      <!-- footer bottom -->
      <section>
        
      </section>

    </div>

  </footer>

</template>

<style scoped>

/* general */
.flex{
  display: flex;
  justify-content: space-between;
  align-items: center;
}

img{
  max-width: 100%;
}

.bg-blue{
  background-color: #0082F9;
}

.bg-black{
  background-color: #0E0E0E;
}

a{
  text-decoration: none;
  display: inline-block;

  padding: 10px;
}

/* header */

.logo{
  width: 60px;
}

.black-section{
height: 50px;
width: 100%;
}

ul{
  padding: 0;

  list-style: none;

  display: flex;
  justify-content: center;
  align-items: center;
}

li .header-link{
  font-family: "Roboto Condensed";
  font-weight: bold;
  font-size: 0.9rem;

  color: rgb(67, 67, 67);

  padding-bottom: 30px;
  margin-top: 30px;

  transition: color 0.3s ease-in-out
}

.header-link.active,
.header-link:hover{
  padding-bottom: 26px;
  color: #0082F9;
  border-bottom: 4px solid #0082F9;
}

/* content */

.content{
  font-size: 1.2rem;

  color: white;

  height: 100px;
}

/* prodotti */

.product-container{
  padding: 15px;
}

.product-container > *{
  color: white;
  margin: 5px;
  font-size: 0.8rem;
}

.product-img{
  height: 35px;
}

</style>
