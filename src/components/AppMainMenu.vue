<script>
export default {
    data() {
        return {
            mainMenu : [
                {
                    icon: "buy-comics-digital-comics.png",
                    text: "digital comics",
                },
                {
                    icon: "buy-comics-merchandise.png",
                    text: "dc merchandise",
                },
                {
                    icon: "buy-comics-subscriptions.png",
                    text: "subscription",
                },
                {
                    icon: "buy-comics-shop-locator.png",
                    text: "comic shop locator",
                },
                {
                    icon: "buy-dc-power-visa.svg",
                    text: "dc power visa",
                }
            ],

        };
    },
    methods: {
        getImage(img) {
      return new URL(`../../public/img/${img}`, import.meta.url).href
    }
    }
}
</script>

<template>

    <main>

       <div class="container">
            <nav>
                <ul>
                    <li v-for="(menu, index) in mainMenu" :key="index">
                        <div class="icon">
                            <img :src="getImage(menu.icon)"/>
                        </div>
                        <a>{{ menu.text }}</a>
                    </li>
                </ul>
            </nav>         
       </div>

    </main>

</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/variables" as *;

main {
    background-color: $primary-color;
  .container {
    padding : 60px 0;
    
    ul {
      display: flex;
      justify-content: space-around;

      li {
        display: flex;
        
        .icon {
          display: flex;
          align-items: center;
          justify-content: center;
          height: 50px;

          img {
            max-height: 100%;
          }
        }
        .icon {
            width : 60px;
        }

        a {
          text-transform: uppercase;
          color: white;
          padding-left : 15px;
          text-decoration: none;
          line-height: 50px;

          &:hover {
            text-decoration: underline;
          }
        }
      }
    }
  }
}

</style>