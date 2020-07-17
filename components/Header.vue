<template lang="html">
  <header class="header">
      <div class="container">
          <div class="header__wrap">
              <app-logo/>
              <Menu/>
              <a :href="`tel:${phone}`" class="header__link">{{phone}}</a>
              <button type="button" name="button" class="btn">{{btnText}}</button>
          </div>
      </div>

  </header>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'
import Menu from '~/components/Menu.vue'


export default {
    components: {
        AppLogo,
        Menu
    },
    data() {
        return {
            phone: '+38(095) 13 87 167',
            btnText: 'Консультация'
        }
    }
}
</script>

<style lang="scss" scoped>
    .header {
        // background: linear-gradient(to top, #252897, #5458BF);
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        padding: 50px 0 0;
        z-index: 2;

        &__wrap {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        &__link {
            text-decoration: none;
            color: #fff;
            font-size: 19px;
            margin-right: 3%;
            white-space: nowrap;
        }
    }
</style>
