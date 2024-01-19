<script>
export default {
    data() {
        return {
        };
    },
    props: {
        thumb: String,
        series: String
    }
}
</script>

<template>
    <div class="card">
        <div class="thumb">
            <img :src="thumb" :alt="series">
        </div>
        <h5>{{ series }}</h5>
    </div>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/variables" as *;
@use "../assets/scss/partials/mixins.scss" as *;
.card {
    width: calc(100% / 6);
    padding: 0 10px;

    .thumb {
      margin-bottom: 20px;
      overflow: hidden;
      height: 220px;
      position: relative;
         
      img {
        width: 100%;
        position: absolute;
        margin: auto;
        top: 0px;
        left: 0;
        right: 0;
        bottom: 0;
        }
    }

    h5 {
        @include uppercase;
        margin-bottom: 50px;
    }
}
</style>