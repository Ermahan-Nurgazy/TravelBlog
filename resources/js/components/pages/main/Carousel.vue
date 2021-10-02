<template>
    <div id="carouselExampleControls" class="carousel slide carousel-fade full-width-div" data-ride="carousel">
        <div class="carousel-inner" style="height: 500px;">
            <div class="carousel-item active">
                <img :src="require('../../img/1.jpg').default" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
                <img :src="require('../../img/2.jpg').default" class="d-block w-100" alt="...">
            </div>
            <div class="carousel-item">
                <img :src="require('../../img/3.jpg').default" class="d-block w-100" alt="...">
            </div>
        </div>
        <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only"></span>
        </a>
        <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only"></span>
        </a>
    </div>
</template>

<script>
export default {
    name: "Carousel"
}
</script>

<style scoped>

</style>
