<script>
export default {
    data() {
        return {

            footerMenu : {

                dcComics : [
                    "dc comics",
                    {
                    href: "#",
                    text: "characters",
                    },
                    {
                    href: "#",
                    text: "comics",
                    },
                    {
                    href: "#",
                    text: "movies",
                    },
                    {
                    href: "#",
                    text: "tv",
                    },
                    {
                    href: "#",
                    text: "games",
                    },
                    {
                    href: "#",
                    text: "videos",
                    },
                    {
                    href: "#",
                    text: "news",
                    }
                ],

                shop: [
                    "shop",
                    {
                    href: "#",
                    text: "Shop DC",
                    },
                    {
                    href: "#",
                    text: "Shop DC Collectibles",
                    }
                ],

                dc: [
                    "dc",
                    {
                    href: "#",
                    text: "Terms Of Use",
                    },
                    {
                    href: "#",
                    text: "Privacy Policy (New)",
                    },
                    {
                    href: "#",
                    text: "Ad Choices",
                    },
                    {
                    href: "#",
                    text: "Advertising",
                    },
                    {
                    href: "#",
                    text: "Jobs",
                    },
                    {
                    href: "#",
                    text: "Subscriptions",
                    },
                    {
                    href: "#",
                    text: "Talent Workshops",
                    },
                    {
                    href: "#",
                    text: "CPSC Certificate",
                    },
                    {
                    href: "#",
                    text: "Rating",
                    },
                    {
                    href: "#",
                    text: "Shop Help",
                    },
                    {
                    href: "#",
                    text: "Contact Us",
                    }
                ],

                sites: [
                    "sites",
                    {
                    href: "#",
                    text: "DC",
                    },
                    {
                    href: "#",
                    text: "Mad Magazine",
                    },
                    {
                    href: "#",
                    text: "DC Kids",
                    },
                    {
                    href: "#",
                    text: "DC Universe",
                    },
                    {
                    href: "#",
                    text: "DC Power Visa",
                    }
                ]
            }

        };
    },
    methods: {

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
                            <a :href="item.href">{{ item.text }}</a>
                        </li>
                    </ul>
                </div>

                <div class="bg-logo">
                    <img src="../../public/img/dc-logo-bg.png" alt="logobg">
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

</style>