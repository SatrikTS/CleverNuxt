<template lang="html">
    <div class="portfolio-card">
        <div class="container">
            <div class="portfolio-card__wrap">
                <div class="portfolio-card__pictures">
                    <div class="portfolio-card__pictures-big">
                        <img src="~assets/img/test1.jpg">
                    </div>
                    <div class="portfolio-card__pictures-small">
                        <img src="~assets/img/test2.jpg">
                    </div>
                </div>
                <div class="portfolio-card__data">
                    <span class="portfolio-card__title">{{item.title}}</span>
                    <div class="portfolio-card__info">
                        <span class="portfolio-card__item" v-for="(item, key) in item.optionsList" :key="key">
                            <span class="portfolio-card__key">{{key}}</span>
                            <span class="portfolio-card__value">{{item}}</span>
                        </span>
                    </div>
                    <nuxt-link :to="item.path" class="btn">Открыть кейс</nuxt-link>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['item']
}
</script>

<style lang="scss" scoped>
    .portfolio-card {
        background: $light-bg;
        padding: $spacer * 6 0 0;
        margin: 0 0 $spacer * 20;
        color: #000;

        &__pictures {
            max-width: 60%;
            flex: 0 0 60%;
            position: relative;
            padding-right: 7%;

            img {
                max-width: 100%;
            }
        }

        &__pictures-small {
            position: absolute;
            width: 386px;
            height: 267px;
            top: 100px;
            right: 0;
            box-shadow: 2px 7px 14px 3px #afabc6;
            border: 15px solid #fff;

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }

        &__pictures-big {
            height: 355px;
            margin-bottom: - $spacer * 10;
            box-shadow: 2px 7px 14px 3px #afabc6;

            img {
                width: 100%;
                height: 100%;
            }
        }

        &__title {
            color: $text-dark;
            font-size: $font-size-xxl;
            font-weight: bold;
            margin: 0 0 $spacer * 10;
        }

        &__wrap {
            display: flex;
        }

        &__data {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            max-width: 40%;
            flex: 0 0 40%;
            padding: 0 7%;
        }

        &__info {
            display: flex;
            flex-direction: column;
            margin: 0 0 $spacer * 8;
        }

        &__item {
            font-size: $font-size-lg;
            margin: 0 0 $spacer;
        }

        &__key {
            color: $text-grey;
        }

        &__value {
            color: $text-dark;
        }

        .btn {
            text-decoration: none;
        }
    }
</style>
