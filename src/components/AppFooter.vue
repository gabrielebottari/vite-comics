<script>
export default {
    data() {
        return {

            footerMenu : {

                dcComics : [
                    "dc comics",
                    {
                    text: "characters",
                    },
                    {
                    text: "comics",
                    },
                    {
                    text: "movies",
                    },
                    {
                    text: "tv",
                    },
                    {
                    text: "games",
                    },
                    {

                    text: "videos",
                    },
                    {
                    text: "news",
                    }
                ],

                shop: [
                    "shop",
                    {
                    text: "Shop DC",
                    },
                    {
                    text: "Shop DC Collectibles",
                    }
                ],

                dc: [
                    "dc",
                    {
                    text: "Terms Of Use",
                    },
                    {
                    text: "Privacy Policy (New)",
                    },
                    {
                    text: "Ad Choices",
                    },
                    {
                    text: "Advertising",
                    },
                    {
                    text: "Jobs",
                    },
                    {
                    text: "Subscriptions",
                    },
                    {
                    text: "Talent Workshops",
                    },
                    {
                    text: "CPSC Certificate",
                    },
                    {
                    text: "Rating",
                    },
                    {
                    text: "Shop Help",
                    },
                    {
                    text: "Contact Us",
                    }
                ],

                sites: [
                    "sites",
                    {
                    text: "DC",
                    },
                    {
                    text: "Mad Magazine",
                    },
                    {
                    text: "DC Kids",
                    },
                    {
                    text: "DC Universe",
                    },
                    {
                    text: "DC Power Visa",
                    }
                ]
            },

            socialMenu : [
                {
                    name: "Facebook",
                    image: "footer-facebook.png",
                },
                {
                    name: "Twitter",
                    image: "footer-twitter.png",
                },
                {
                    name: "YouTube",
                    image: "footer-youtube.png",
                },
                {
                    name: "Pinterest",
                    image: "footer-pinterest.png",
                },
                {
                    name: "Periscope",
                    image: "footer-periscope.png",
                },
            ]

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
    <footer>
        <div class="footer-top">
            <div class="container">
                <div v-for="(section, sectionTitle) in footerMenu" :key="sectionTitle" class="menu">
                    <h3>{{ section[0] }}</h3>
                    <ul>
                        <li v-for="(item, index) in section.slice(1)" :key="index">
                            <a>{{ item.text }}</a>
                        </li>
                    </ul>
                </div>

                <div class="bg-logo">
                    <img src="../../public/img/dc-logo-bg.png" alt="logobg">
                </div>
            </div>
        </div>

        <div class="bottom">
            <div class="container">
                <button>Sign-Up Now!</button>
                <div class="social">
                     <h3>Follow Us</h3>
                    <ul>
                        <li v-for="(social, index) in socialMenu" :key="index">
                            <a :href="social.href"><img class="social-logo" :src="getImage(social.image)" :alt="social.name"></a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/variables.scss" as *;
.footer-top {
    background-image: url("../public/img/footer-bg.jpg");
    background-size: cover;
    height: 275px;
    position: relative;
    overflow: hidden;

    .container {
      padding: 20px 0;
      display: flex;

      .menu {
        padding-right: 20px;

        h3 {
          color: white;
          text-transform: uppercase;
          margin-bottom: 10px;
        }
  
        ul {
            list-style: none;
          li {
            a {
              text-transform: capitalize;
              color: gray;
              list-style: none;
              text-decoration: none;
              
              &:hover {
                text-decoration: underline;
              }
            }
          }
        }
      }
      .bg-logo {
        position: absolute;
        top: -120px;
        right : 200px;
      }
      
    }
  }
  .bottom {
    padding: 30px 0;
    background-color: #303030;

    .container {
        display: flex;
        align-content: center;
        justify-content: space-between;
        text-transform: uppercase;

        button {
            border: 2px solid $primary-color;
            color: white;
            padding: 15px 20px;
            background-color: transparent;
            text-transform: uppercase;
        }
        .social {
            display: flex;
            align-content: center;

            h3 {
                color: $primary-color;
                padding: 0 10px;
                align-self: center;
            }

            ul {
                display: flex;
                align-self: center;
                list-style: none;
                li {
                    padding: 0 10px;
                }
            }
        }
    }
  }

</style>