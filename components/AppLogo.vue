<template>
  <div class="logo">
    <span class="logo__figure">

    </span>
    <span class="logo__circle"></span>
    <span class="logo__text">
        Clever Digital Agency
    </span>
  </div>
</template>



<style lang="scss" scoped>

.logo {
    display: flex;
    align-items: center;
    position: relative;

    &__circle {
        position: absolute;
        width: 20px;
        height: 20px;
        background: #00FFFF;
        left: 8.7px;
        top: 10.5px;
        border-radius: 100%;
        box-shadow: 0px 0px 9px 4px #6d71c5;
        animation: logoColor 4s linear infinite;
    }


    &__figure {
        border: 1px solid #00FFFF;
        border-radius: 100%;
        min-width: 37px;
        min-height: 37px;
        position: relative;
        padding: 10px;
        //animation: orbitRotate 20s linear infinite;

        &::after {
            position: absolute;
            content: '';
            width: 7px;
            height: 7px;
            background: #fff;
            border-radius: 100%;
            top: 13.5px;
            right: 13px;
            animation: myOrbit 4s linear infinite;
        }

    }

    &__text {
        font-size: 14px;
        line-height: 1;
        max-width: 70px;
        margin-left: 7px;
        font-weight: 500;
    }
}

@keyframes myOrbit {
    from { transform: rotate(0deg) translateX(18px) rotate(0deg); }
    to   { transform: rotate(360deg) translateX(18px) rotate(-360deg); }
}

@keyframes orbitRotate {
    from { transform: rotateX(0deg)}
    to   { transform: rotateX(360deg)}
}

@keyframes logoColor {
    0% {
        background: #fff;
    }
    50%   {
        background: #00FFFF;
    }
    100%   {
        background: #fff;
    }
}

</style>
