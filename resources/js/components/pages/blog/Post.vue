<template>
    <div class="col mb-4">
        <div class="card" >
            <img :src="require('../../img/1.jpg').default" class="card-img-top" alt="...">
            <div class="card-body">
                <h5 class="card-title">{{ title }}</h5>
                <p class="card-text">{{ body }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            default: "NULL"
        },
        body: {
            type: String,
            default: "NULL"
        }
    }
}
</script>

<style scoped>

</style>
