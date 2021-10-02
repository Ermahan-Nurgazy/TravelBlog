<template>
    <div id="app">
        <spin v-if="loading"></spin>
        <div v-else>
            <div class="container my-lg-5">
                <div class="row row-cols-1 row-cols-md-2">
                    <post
                        v-for="post in posts"
                        :title="post.title"
                        :body="post.body"
                    />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Spin from "../components/Spin";
    import axios from 'axios';
    import Post from "../components/pages/blog/Post";

    export default {
        components: {
            Spin,
            Post
        },
        data: () => ({
            loading: true,
            posts: []
        }),
        mounted() {
            this.loadPosts();
        },
        methods: {
            loadPosts (){
                axios.get('/api/posts')
                .then( res => {
                    this.posts = res.data;
                    setTimeout(() => {
                        this.loading = false;
                    },500)
                })
            }
        }
    }
</script>

<style scoped>

</style>
