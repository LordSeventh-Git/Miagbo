<template lang="html">
    <footer class="ps-footer">
        <div class="ps-container row">
            <!--<FooterWidgets />-->
            <div class="col-6 col-md-3">
                <ul class="footer__else">
                    <li class="footer__else__li">Acheter sur Miagbo</li>
                    <li>aaaaaaaaa</li>
                    <li>aaaaaaaaaaaaaa</li>
                    <li>aaaaaaa</li>
                </ul>
            </div>
            <div class="col-6 col-md-3">
                <ul class="footer__else">
                    <li class="footer__else__li">Vendre sur Miagbo</li>
                    <li>Conditions d'utilisation</li>
                    <li>Conditions d'utilisation</li>
                    <li>Conditions d'utilisation</li>
                </ul>
            </div>            
            <FooterLinks class="col-6 col-md-3" />
            <FooterCopyright class="col-6 col-md-3" />
        </div>
        <div class="footer__social">
            <ul class="ps-list--social">
                <li>
                    <a class="facebook" href="https://www.facebook.com/miagbo/">
                        <i class="fa fa-facebook"></i>
                    </a>
                </li>                    
                <li>
                    <a class="instagram" href="https://instagram.com/miagbo.tg?igshid=rep561mrp6uv">
                        <i class="fa fa-instagram"></i>
                    </a>
                </li>
                <li>
                    <a class="twitter" href="https://twitter.com/miagbo">
                        <i class="fa fa-twitter"></i>
                    </a>
                </li>
                <li>
                    <a class="linkedin" href="https://www.linkedin.com/company/miagbo">
                        <i class="fa fa-linkedin" style="color: #0073B1;"></i>
                    </a>
                </li>
                <li>
                    <a class="mail" href="mailto:info@centech-togo.com">
                        <i class="fa fa-envelope"></i>
                    </a>
                </li>
            </ul>
        </div>
        <div>
            <p v-html="$t('footer.copyright')" class="ps-footer__copyright__other">

            </p>
        </div>
    </footer>
</template>
<script>
import FooterWidgets from '~/components/shared/footers/modules/FooterWidgets';
import FooterCopyright from '~/components/shared/footers/modules/FooterCopyright';
import FooterLinks from '~/components/shared/footers/modules/FooterLinks';

export default {
    components: {
        FooterWidgets,
        FooterCopyright,
        FooterLinks
    }
};
</script>
<style lang="scss" scoped>
.footer__else{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.footer__else__li {
    font-weight: 700;
    font-size: 1.2em;
}
.footer__else * {
    color: white;
}
.footer__else li{
    list-style: none;
    margin: 10px;
}
.ps-footer{
    background-color: #14261a;
}
.ps-container{
    display: flex;
    justify-content: space-around;
}
.footer__social{
    display: flex;
    justify-content: center;
    margin-bottom: 5px;
}
.ps-footer__copyright__other{
    display: flex;
    color: white;
    justify-content: center;
    padding-bottom: 70px;
    margin-bottom: 0;
}
</style>
