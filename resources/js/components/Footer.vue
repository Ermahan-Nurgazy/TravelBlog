<template>
    <div class="footer mt-lg-5" style=" bottom: 0; min-width: 100%;">
        <div class="bg-dark">
            <div class="container">
                <div class="row p-1">
                    <div class="col-6 mt-lg-3 text-white-50">
                        <p>MALGAZHDAR.ERMAHAN@GMAIL.COM <br> +7-705-656-92-01</p>
                    </div>
                    <div class="col-4 mt-lg-3">
                        <a class="navbar-brand text-white " style="text-decoration: none;" href="#">ГУЛЯЙ!</a>
                        <p class="text-white-50" style="margin-left: -12%;">ALL RIGHTS RESERVED</p>
                    </div>
                    <div class="col-2 mt-lg-3">
                        <img :src="require('./img/vk.svg').default" style="height: 30px; width: 30px;" alt="">
                        <img :src="require('./img/instagram.svg').default" style="height: 30px; width: 30px;" alt="">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style scoped>

</style>
