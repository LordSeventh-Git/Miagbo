<template lang="html">
    <div>
        <ul class="footer__ul">
            <li class="footer__ul__li">Conditions d'utilisation de Miagbo</li>
            <li><a href="">lorem lorem lorem lorem lorem lorem</a></li>
            <li><a href="">lorem lorem lorem lorem lorem lorem</a></li>
            <li><a href="">lorem lorem lorem lorem lorem lorem</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'FooterLinks',
    data() {
        return {}
        }
            
};
</script>
<style lang="scss" scoped>
.footer__ul{
    display: flex;
    flex-direction: column;
}
.footer__ul *{
    color: white;
}
.footer__ul > li {
    list-style: none;
    margin: 10px;
}
.footer__ul__li{
    font-weight: 700;
    font-size: 1.2em;
}
</style>
