<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },
                {
                    text: "TV",
                    url: "#",
                    current: false
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="left">
            <a href="">
                <img src="../assets/img/dc-logo.png" alt="">
            </a>
        </div>
        <nav class="right">
            <ul class="header-nav">
                <li :class="elem.current ? 'active' : ''" v-for="elem in links">{{elem.text}}</li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;
@use "../style/general.scss" as *;


header {
    text-align: center;
    @include flex(row, space-between, center);
    margin: 5px auto;
    width: $width;
    height: 100px;
    font-size: .8rem;
    .right {
        margin: 2rem 0;
        
        .header-nav {
            list-style: none;
            @include flex(row, center, center);
            li {
                margin: 0 .5rem;
                cursor: pointer;
                position: relative;
                a {
                    color: $text-color;
                    text-decoration: none;
                }
                &.active,
                &:hover {
                    color: $primary;
                    &:after {
                        content: '';
                        position: absolute;
                        bottom: -45px;
                        left: 50%;
                        width: 100%;
                        border-bottom: 4px solid $primary;
                        transform: translate(-50%, 50%);
                    }
                }
            }
        }
    }
};
</style>