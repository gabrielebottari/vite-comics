<script>
export default {
    data() {
        return {
            
            headerMenu : [
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
                text: "collectibles",
                },
                {
                text: "videos",
                },
                {
                text: "fans",
                },
                {
                text: "news",
                },
                {
                text: "shop",
                }
            ],

        };
    },
    methods: {

    }
}
</script>

<template>

  <header>

    <div class="container">

        <div class="logo">
            <img src="../../public/img/dc-logo.png" alt="Logo" />
        </div>
        <nav>
            <ul>
                <li v-for="item in headerMenu" :key="item.text">
                    <a>{{ item.text }}</a>
                </li>
            </ul>
        </nav>

    </div>

  </header>

</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/variables.scss" as *;

header {
    .container {
        display: flex;
        justify-content: space-between;
        height: 120px;
      
        .logo {
        height : 100%;
        padding : 20px 0;
        vertical-align: middle;

            img {
            max-height: 100%;
            }
        }
  
        nav {
            height: 100%;
            vertical-align: middle;

            ul {
                display: flex;
                height : 100%;
                list-style: none;
                li {
                    padding: 0 10px;
                    align-self: center;
  
                    a {
                        height : 100%;
                        text-transform: uppercase;
                        text-decoration: none;
                        color: #1C1C1C;
                        padding : 45px 0px;
                        border-bottom: 5px solid transparent;

                        &:hover {
                        color : $primary-color;
                        border-bottom: 5px solid $primary-color;
                        }
                    }
                }
            }
        }
    }
  }
</style>