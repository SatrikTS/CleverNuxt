<template lang="html">
    <nav class="menu">
      <li class="menu__item" v-for="item in menuItem"  v-bind:key="item.id">
          <a class="menu__link" :href="item.menuHref">{{item.menuName}}</a>
      </li>
    </nav>
    
</template>

<script>
export default {
    data() {
        return {
            menuItem: [
                {
                    menuName: 'Главная',
                    menuHref: '#'
                },
                {
                    menuName: 'Услуги',
                    menuHref: '#'
                },
                {
                    menuName: 'Портфолио',
                    menuHref: '#'
                },
                {
                    menuName: 'Контакты',
                    menuHref: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .menu {
        list-style: none;
        display: flex;
        align-items: center;
        flex: 1;
        justify-content: space-between;
        padding: 0 30px;
        max-width: 470px;

        &__link {
            color: #fff;
            font-size: 19px;
            text-decoration: none;
        }
    }
</style>
