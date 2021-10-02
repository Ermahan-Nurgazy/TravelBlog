<template>
    <div id="app">
        <spin v-if="loading"/>
        <div class="media p-lg-5 d-flex" v-else-if="!loading && !not_found">
            <div>
                <img :src="require('../components/img/1.jpg').default" class="align-self-center p-3" style="width: 400px;" alt="...">
            </div>
            <div class="media-body">
                <h5 class="mt-3">{{ post.title }}</h5>
                <p>{{ post.body }}</p>
            </div>
            <div class="alert alert-danger" role="alert" v-if="not_found">
                Пост не найден!
            </div>
        </div>
    </div>
</template>

<script>
import Spin from "../components/Spin";
import axios from "axios";

export default {
    components: {
        Spin
    },
    data: () => ({
       loading: true,
       post: [],
       not_found: false
    }),
    mounted() {
        this.loadPost(this.$route.params.id)
    },
    methods: {
        loadPost(id) {
            axios.get('/api/posts/' + id)
            .then(res => {
                this.post = res.data;
                setTimeout(() => {
                    this.loading = false;
                },500);
            })
            .catch(err => {
                this.not_found = true;
            })
        }
    }
}
</script>

<style scoped>

</style>
