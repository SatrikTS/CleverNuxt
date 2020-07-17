<template lang="html">
    <div class="banner">
        <div class="banner__wrap"></div>
        <div class="container">
                <h1 class="header-title">{{title}}</h1>
                <Services/>
        </div>
        <div class="banner__img">
            <img src="~assets/img/maintenance.png">
        </div>
    </div>
</template>

<script>
    import Services from '~/components/Services.vue'

    export default {
        components: {
            Services
        },
        data() {
            return {
                title: 'Создаем эффектные и эффективные решения для вашего бизнеса'
            }
        }
    }
</script>

<style lang="scss" scoped>
    .banner {
        // min-height: 100vh;
        // min-height: 722px;
        display: flex;
        padding: $spacer * 44 0;
        margin: 0 0 $spacer * 30;
        position: relative;

        &__wrap {
            min-height: 100vh;
            min-height: 722px;
            background: linear-gradient(to top, $primary-dark, $primary-light);
            clip-path: polygon(0 0, 100% 0%, 100% 88%, 0 99.5%);
            clip-path: polygon(0 0, 100% 0%, 100% 100%, 0 86%);
            width: 100%;
            position: absolute;
            top: 0;

            &::before {
                content: '';
                position: absolute;
                width: 100%;
                height: 100%;
                left: 0;
                top: 0;
                background: url('~assets/img/line.png') no-repeat center;
                background-size: 190% 110%;
            }
        }

        &__img {
            position: absolute;
            z-index: 3;
            right: 0;
            bottom: -200px;
            max-width: 670px;

            img {
                max-width: 100%;
            }
        }
    }
</style>
