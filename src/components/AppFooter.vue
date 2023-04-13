<script>
export default {
    name: "AppFooter",
    data() {
        return {
            footerLinks: {
                "dc comics": [
                    {
                        name: "characters",
                        url: "#"
                    },
                    {
                        name: "Comics",
                        url: "#"
                    },
                    {
                        name: "Movies",
                        url: "#"
                    },
                    {
                        name: "TV",
                        url: "#"
                    },
                    {
                        name: "Games",
                        url: "#"
                    },
                    {
                        name: "Videos",
                        url: "#"
                    },
                    {
                        name: "News",
                        url: "#"
                    },
                ],
                "dc": [
                    {
                        name: "Terms of Use",
                        url: "#"
                    },
                    {
                        name: "Privacy policy(New)",
                        url: "#"
                    },
                    {
                        name: "Ad Choices",
                        url: "#"
                    },
                    {
                        name: "Adverstring",
                        url: "#"
                    },
                    {
                        name: "Jobs",
                        url: "#"
                    },
                    {
                        name: "CPSC Certificates",
                        url: "#"
                    },
                    {
                        name: "Subscriptions",
                        url: "#"
                    },
                    {
                        name: "Talent Workshops",
                        url: "#"
                    },
                    {
                        name: "Ratings",
                        url: "#"
                    },
                    {
                        name: "Shop Help",
                        url: "#"
                    },
                    {
                        name: "Contact Us",
                        url: "#"
                    },
                ],
                "sites": [
                    {
                        name: "DC",
                        url: "#"
                    },
                    {
                        name: "MAD Magazine",
                        url: "#"
                    },
                    {
                        name: "DC Kids",
                        url: "#"
                    },
                    {
                        name: "DC Universe",
                        url: "#"
                    },
                    {
                        name: "DC Power Visa",
                        url: "#"
                    },
                ],
                "shop": [
                    {
                        name: "Shop DC",
                        url: "#"
                    },
                    {
                        name: "Shop DC Collectables",
                        url: "#"
                    },
                ]
            },
            socialImg: [
                {
                    img: "./src/assets/img/footer-facebook.png",
                    url: "https://it-it.facebook.com"
                },
                {
                    img: "./src/assets/img/footer-twitter.png",
                    url: "#"
                },
                {
                    img: "./src/assets/img/footer-youtube.png",
                    url: "#"
                },
                {
                    img: "./src/assets/img/footer-pinterest.png",
                    url: "#"
                },
                {
                    img: "./src/assets/img/footer-periscope.png",
                    url: "#"
                },
            ]
        }
    },
}
</script>

<template>
    <footer>
        <div class="top">
            <div class="left">
                <div v-for="(elem, index) in footerLinks" class="card">
                    <h2> {{ index }} </h2>
                    <ul>
                        <li v-for="link in elem">
                            <a :href="link.url">{{ link.name }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="right">
                <img class="footer-logo" src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
        <div class="bottom">
            <div class="container">
                <button>SIGN-UP NOW!</button>
                <ul>
                    <li><a href="">FOLLOW US</a></li>
                    <li v-for="elem in socialImg">
                        <a :href="elem.url">
                            <img :src="elem.img" alt="">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;
@use "../style/general.scss" as *;

footer {
    height: 500px;
    z-index: -1;
    background-image: url(../src/assets/img/footer-bg.jpg);
    background-size: cover;
    .top {
        height: 100%;
        position: relative;
        margin: 0 auto;
        width: $width;
        .left {
            width: 500px;
            display: flex;
            flex-wrap: wrap;
            .card {
                width: calc(100% / 3);
            }
            h2 {
                text-transform: uppercase;
                color: white;
                font-size: .6rem;
                margin-top: 1rem;
            }
            ul {
                list-style-type: none;
                padding-top: .4rem;
                a {
                    color: rgba(255, 255, 255, 0.288);
                    text-decoration: none;
                    font-size: .6rem;
                }
            }
        }
        .right {
            height: 100%;
            position: absolute;
            top: 0;
            left: 60%;
            img {
                height: 100%;
                width: 100%;
                transform: scale(1.2);
                display: block;
                z-index: 0;
            }
        }
    }
    .bottom {
        position: relative;
        background-color: $dark_bg_color;
        z-index: 10;
        height: 150px;
        .container {
            height: 100%;
            margin: 0 auto;
            width: $width;
            display: flex;
            justify-content: space-between;
            align-items: center;
            button {
                color: white;
                background-color: inherit;
                border: none;
                padding: .8rem .6rem;
                border: 1px solid $primary;
                cursor: pointer;
            }
            ul {
                display: flex;
                list-style-type: none;
                li {
                    &:first-child {
                        font-size: .7rem;
                        font-weight: 600;
                    }
                    line-height: 150px;
                    margin-right: 1rem;
                }
                a {
                    text-decoration: none;
                    color: $primary;
                    img {
                        vertical-align: middle;
                        width: 25px;
                    }
                }
            }
        }
    }
    img {
        max-width: 100%;
        max-height: 100%;
    }
}
</style>