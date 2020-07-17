<template>
    <main>
        <Header/>
        <Banner/>
        <Offer/>
        <Portfolio/>
    </main>
</template>

<script>

import Header from '~/components/Header.vue'
import Banner from '~/components/Banner.vue'
import Offer from '~/components/Offer.vue'
import Portfolio from '~/components/Portfolio.vue'

export default {
    components: {
      Header,
      Banner,
      Offer,
      Portfolio
    },
    data() {
        return {
            title: 'asd'
        }
    }
}
</script>

<style>

</style>
