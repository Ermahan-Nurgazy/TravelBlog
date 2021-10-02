<template>
    <div id="app" class="container">
        <form class="my-lg-5">
            <div class="alert alert-danger" role="alert" v-if="error">
                Проверьте правильность введенных полей!
            </div>
            <h3>Опубликовать блог</h3>
            <div class="form-group mb-3">
                <input type="text" class="form-control" v-model="form.title" placeholder="Введите название">
            </div>
            <div class="form-group mb-3">
                <textarea class="form-control" v-model="form.body" rows="3" placeholder="Введите информацию"></textarea>
            </div>
            <button class="btn btn-primary" @click.prevent="store">
                <div class="spinner-border text-light" role="status" v-if="loading"></div>
                <span v-else>Опубликовать</span>
            </button>
        </form>
    </div>
</template>

<script>
import axios from "axios";

export default {
    components: {},
    data: () => ({
        form: {
            title: "",
            body: "",
        },
        loading: false,
        error: false
    }),
    mounted() {

    },
    methods: {
        store () {
            this.loading = true;
            axios.post('/api/posts', this.form, {
                headers: {
                    "Content-type" : "application/json"
                }
            })
            .then(res => {
                if (res.data.status) {
                    this.$router.push('/posts/' + res.data.post.id);
                } else {
                    setTimeout(this.loading = false);
                    this.error = true;
                }
            })
            .catch(err => {
                console.log(err.response.data)
            })
        }
    }
}
</script>

<style scoped>

</style>
