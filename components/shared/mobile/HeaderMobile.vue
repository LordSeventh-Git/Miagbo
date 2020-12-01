<template lang="html">
    <header class="header header--mobile">
        <!--<div class="header__top">
            <div class="header__left">
                <p>Bienvenue sur Miagbo</p>
            </div>
            <div class="header__right">
                <ul class="navigation__extra">
                    <li>
                        <nuxt-link to="/vendor/become-a-vendor">
                            Devenir un vendeur
                        </nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/account/order-tracking">
                            Etat de votre commande
                        </nuxt-link>
                    </li>
                </ul>
            </div>
        </div>-->
        <div class="navigation--mobile">
            <div class="navigation__left">
                <nuxt-link to="/" class="ps-logo">
                    <img src="~/static/img/logo_miagbo.png"  style="height:70px;width:70px;" alt="miagbo" />
                </nuxt-link>
            </div>


            <span id="logo_font">Miagbo</span>


            <mobile-header-actions />
        </div>
    </header>
</template>

<script>
import MobileHeaderActions from '~/components/shared/mobile/modules/MobileHeaderActions';
export default {
    name: 'HeaderMobile',
    components: { MobileHeaderActions }
};
</script>

<style lang="scss" scoped>
@font-face {
    font-family: "Ghoust Solid";
    src: url("/assets/scss/modules/Ghoust_Solid.otf") format("otf");
}
#logo_font{
    font-family: "Ghoust Solid";
    font-size: 40px;
    text-align: center;
    margin-top: 7px;
    margin-left: -20px;
}
</style>
