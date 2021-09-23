<template>
    <div class="container">
        <div class="my-lg-5">
            <div class="row no-gutters">
                <div class="col-md-4">
                    <img :src="require('../../img/4.jpg').default" class="card-img h-70" style="border-radius: 10px;" alt="...">
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                        <h3 class="card-title">Привет, меня зовут Ермахан!</h3>
                        <p class="card-text mt-4" style="font-size: 24px;">Мой блог о путешествиях – жизнь в стиле трэвел. Увидеть весь мир – вот мечта и план-максимум каждого путешественника. Для меня каждое путешествие – это увлекательное приключение, полное романтизма и удовольствия от новых открытий. На страницах своего блога я рассказываю о своих путешествиях, которые мне удалось совершить в прошлом, которые я совершаю в настоящее время.</p>
                        <button type="button" class="btn btn-outline-dark mt-auto ml-auto">СМОТРЕТЬ БЛОГИ &#8594;</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "AboutMe"
}
</script>

<style scoped>

</style>
