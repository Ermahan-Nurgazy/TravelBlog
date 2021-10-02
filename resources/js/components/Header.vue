<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container">
            <div>
                <router-link class="navbar-brand" to="/">ГУЛЯЙ!</router-link>
            </div>
            <div>
                <ul class="navbar-nav">
                    <li v-for="link in links" class="nav-item">
                        <router-link class="nav-link" :to="link.href">{{ link.title }}</router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    data () {
        return {
            links: [
                {
                    title: "БЛОГ",
                    href: "/blog"
                },
                {
                    title: "АВТОРИЗОВАТЬСЯ",
                    href: "/auth"
                },
                {
                    title: "СОЗДАТЬ ПОСТ",
                    href: "/create"
                }
            ]
        }
    }
}
</script>

<style scoped>

</style>
