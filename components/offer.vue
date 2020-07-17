<template lang="html">
    <div class="offer">
        <div class="container">
            <h2 class="title">Услуги</h2>
            <div class="offer__wrap">
                <div class="offer-item" v-for="(item, index) in offerList" :key="index">
                    <span class="offer-item__caption">{{item.title}}</span>
                    <span class="offer-item__price">
                        <span v-if="index === 0" class="offer-item__label">
                            Цена
                        </span>
                        {{item.price}}
                    </span>
                    <span class="offer-item__time">
                        <span v-if="index === 0" class="offer-item__label">
                            Срок исполнения
                        </span>
                        {{item.time}}
                    </span>
                    <nuxt-link :to="item.path" class="offer-item__button btn btn--left btn--light">Подробнее</nuxt-link>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            offerList: [
                {
                    title: 'Интернет-магазины' ,
                    price: '2500',
                    time: '1-3 месяца',
                    path: '#'
                },
                {
                    title: 'Корпоративные сайты' ,
                    price: '2500',
                    time: '3 месяца',
                    path: '#'
                },
                {
                    title: 'Аутсорс' ,
                    price: 'по договорености',
                    time: 'по договренности',
                    path: '#'
                },
                {
                    title: 'Веб-приложения' ,
                    price: '2500',
                    time: '2 месяца',
                    path: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .offer {
        margin: 0 0 $spacer * 30;

        &__wrap {
            padding: $spacer * 20 0 0;
        }
    }

    .offer-item {
        display: flex;
        align-items: baseline;
        justify-content: space-between;
        background: linear-gradient(to top, $primary-dark, $primary-light);
        padding: $spacer * 8 $spacer * 25;
        margin: 0 0 $spacer * 4;

        &:first-child {
            clip-path: polygon(0 0, 100% 22%, 100% 100%, 0% 100%);
            padding: $spacer * 16 $spacer * 25 $spacer * 8;
        }

        &__caption {
            font-size: $font-size-xl;
            font-weight: 500;
            width: 25%;
            flex: 0 0 25%;
            white-space: nowrap;
        }

        &__price {
            font-size: $font-size-lg;
            color: $text-light;
            display: flex;
            flex-direction: column;
            position: relative;
            width: 8.333%;
            flex: 0 0 8.333%;
        }

        &__time {
            font-size: $font-size-lg;
            color: $text-light;
            display: flex;
            flex-direction: column;
            position: relative;
            width: 8.333%;
            flex: 0 0 8.333%;
        }

        &__button {
            text-decoration: none;
        }

        &__label {
            color: $faded-color;
            font-size: $font-size-md;
            position: absolute;
            white-space: nowrap;
            top: -40px;
        }


    }
</style>
