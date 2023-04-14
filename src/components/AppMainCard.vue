<script>
export default {
    name: "AppMainCard",
    props: {
        title: String,
        url: String,
        alt: String
    }
}
</script>

<template>
    <div class="card">
        <img :src="url" :alt="alt">
        <h2>{{ title }}</h2>
    </div>
</template>

<style scoped lang="scss">
.card {
    margin-top: 1.4rem;
    width: calc(100% / 6 - 15px);
    color: white;
    img {
        width: 100%;
        height: 140px;
        object-fit: cover;
    }
    h2 {
        padding: 1rem 0;
        font-size: .8rem;
        font-weight: 300;
    }
}
</style>