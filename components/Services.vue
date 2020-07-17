<template lang="html">
    <div class="services">
            <a :href="item.servicesLink" class="services__item" v-for="item in services"  v-bind:key="item.id">
                <span class="services__item-gear">
                    <!-- <svg class="services__svg">
                        <use :xlink:href="iconGear"></use>
                    </svg> -->
                    <img src="~assets/icons/icon-wheel.svg" alt="" ref="" class="services__img services__img--big">
                    <img src="~assets/icons/icon-wheel.svg" alt="" ref="" class="services__img services__img--small">
                </span>
                <span class="services__item-caption">{{item.servicesName}}</span>
            </a>
    </div>
</template>

<script>
import  iconGear from '~/assets/icons/icon-wheel.svg';

export default {
    data() {
        return {
            iconGear: iconGear,
            services: [
                {
                    servicesName: 'Услуга 1',
                    servicesLink: '#'
                },
                {
                    servicesName: 'Услуга 2',
                    servicesLink: '#'
                },
                {
                    servicesName: 'Услуга 3',
                    servicesLink: '#'
                },
                {
                    servicesName: 'Услуга 4',
                    servicesLink: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .services {
        display: flex;
        justify-content: space-around;
        padding: 88px 0 32px;
        position: relative;

        &__item {
            text-decoration: none;
            font-size: 19px;
            color: #fff;
            margin: 0 0 0;
            display: flex;
            flex-direction: column;
            position: relative;
            z-index: 1;

            &:hover {
                .services__img--small {
                    animation: rotateСlockwise 10s linear infinite;
                }

                .services__img--big {
                    animation: counterСlockwise 20s linear infinite;
                }
            }
        }

        &__item-caption {
            margin: 5px 0 0;
        }

        &__item-gear {
            position: relative;

            &::before {
                position: absolute;
                content: '';
                width: 5px;
                height: 5px;
                background: #11eaf6;
                border-radius: 100%;
                top: 5px;
                left: 45px;
                box-shadow: 0px 0px 13px 6px #6d71c5;
            }
        }

        &__img {
            width: 40px;
            opacity: 0.6;

            &--small {
                width: 20px;
                top: 6px;
                right: 9px;
                position: relative;
            }

            &:hover {
                .services__img--big {
                    background: red;
                }
            }
        }

        &__svg {
            max-width: 40px;
            height: 40px;
        }
    }

    @keyframes rotateСlockwise {
        from { transform: rotate(0deg)}
        to   { transform: rotate(360deg)}
    }

    @keyframes counterСlockwise {
        from { transform: rotate(360deg)}
        to   { transform: rotate(0deg)}
    }

</style>
