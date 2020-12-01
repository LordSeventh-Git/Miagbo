<template lang="html">
<div>    
    <div class="ps-footer__copyright">
        <span>Paiements sécurisés utilisés suivants :</span>
        <p>

            <img src="~/static/img/payment-method/t-money.png" alt="" width="100" height="50" />

    
            <img src="~/static/img/payment-method/flooz2.jpg" alt="" width="100" height="50" />

            <img src="~/static/img/payment-method/visa.png" alt="" width="100" height="50" />


            <img src="~/static/img/payment-method/masterCard.png" alt="" width="100" height="50" />


            <img src="~/static/img/payment-method/western-union.jpg" alt="" width="100" height="50" />

        </p>
    </div>
    <!--<p v-html="$t('footer.copyright')" class="ps-footer__copyright__other">

    </p>-->
</div>
</template>
<script>
export default {
    name: 'FooterCopyright'
};
</script>
<style lang="scss" scoped>
.ps-footer__copyright > span{
    color: white;
}
.ps-footer__copyright > p > img {
    margin: 5px;
}
</style>
