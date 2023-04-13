<script>
export default {
    name: "AppCta",
    data() {
        return {
            cta: [
                {
                    url: './src/assets/img/buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS',
                    alt: 'digital comics icons'
                },
                {
                    url: './src/assets/img/buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE',
                    alt: 'merchandise icons'
                },
                {
                    url: './src/assets/img/buy-comics-subscriptions.png',
                    text: 'SUBSCRIPTION',
                    alt: 'subscription icons'
                },
                {
                    url: './src/assets/img/buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR',
                    alt: 'shopping icons locator'
                },
                {
                    url: './src/assets/img/buy-dc-power-visa.svg',
                    text: 'DC POWER VISA',
                    alt: 'visa icons'
                },
            ]
        }
    },
}
</script>

<template>
    <main>
        <ul>
            <li v-for="elem in cta">
                <img :src="elem.url" alt="">
                <p>{{ elem.text }}</p>
            </li>
        </ul>
    </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;
@use "../style/general.scss" as *;

main {
    background-color: $primary;
    color: white;
    z-index: 999;
}
ul {
    margin: 0 auto;
    padding: 50px 0;
    width: $width;
    list-style-type: none;
    @include flex (row, space-between, center);
    padding: 20px 0;
}

li {
    padding: 10px;
    @include flex (row, space-between, center);
    font-size: .8rem
}
img {
    width: 30px;
}
p {
    margin-left: 5px;
}
</style>