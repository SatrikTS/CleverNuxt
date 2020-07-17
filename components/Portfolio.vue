<template lang="html">
    <div class="portfolio">
        <h2 class="title">Портфолио</h2>
        <div class="portfolio__wrap">
            <PortfolioCard  v-for="(item, index) in cardsData"
             :key="index"
                v-bind:item="item"
                v-bind:index="index"
             />
        </div>
    </div>
</template>

<script>
import PortfolioCard from './PortfolioCard';

export default {
    components: {
        PortfolioCard
    },
    data() {
        return {
            cardsData: [
                {
                    title: 'Title',
                    optionsList: {
                        Тематика: 'Строительство',
                        Тип: 'Интернет-магазин',
                        Срок: '2 месяца'
                    },
                    path: '#'
                },
                {
                    title: 'Title 2',
                    optionsList: {
                        Тематика: 'Финансы',
                        Тип: 'Портал',
                        Срок: '2 месяца'
                    },
                    path: '#'
                },
                {
                    title: 'Title 3',
                    optionsList: {
                        Тематика: 'Кешбек система',
                        Тип: 'Веб-приложение',
                        Срок: '5 месяцев'
                    },
                    path: '#'
                },
                {
                    title: 'Title 4',
                    optionsList: {
                        Тематика: 'Строительство',
                        Тип: 'Сайт',
                        Срок: '1 месяца'
                    },
                    path: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .portfolio {
        .title {
            margin: 0 0 $spacer * 25;
        }
    }
</style>
