<template lang="html">
    <section class="ps-my-account ps-page--account">
        <div class="container">
            <div class="row">
                <div class="col-lg-4">
                    <div class="ps-section__left">
                        <aside class="ps-widget--account-dashboard">
                            <div class="ps-widget__header">
                                <img src="/img/users/3.jpg" />
                                <figure>
                                    <figcaption>Hello</figcaption>
                                    <p>username@gmail.com</p>
                                </figure>
                            </div>
                            <div class="ps-widget__content">
                                <AccountLinks :links="accountLinks" />
                            </div>
                        </aside>
                    </div>
                </div>
                <div class="col-lg-8">
                    <div class="ps-section--account-setting">
                        <div class="ps-section__content">
                            <div class="row">
                                <div class="col-md-6 col-12">
                                    <figure class="ps-block--address">
                                        <!--<figcaption>
                                            Billing address
                                        </figcaption>-->
                                        <figcaption>
                                            Informations de paiement
                                        </figcaption>
                                        <div class="ps-block__content">
                                            <p>
                                                Vous n'avez pas encore fourni vos Informations 
                                                de paiement.
                                            </p>
                                            <nuxt-link
                                                to="/account/edit-address"
                                            >
                                            <button 
                                                style="padding: 10px; margin-bottom: 0;"
                                                type="submit"
                                                class="ps-btn ps-btn--fullwidth"
                                                @click.prevent="handleSubmit"
                                            >
                                                Modifier
                                            </button>
                                            </nuxt-link>
                                        </div>
                                    </figure>
                                </div>
                                <div class="col-md-6 col-12">
                                    <figure class="ps-block--address">
                                        <figcaption>
                                            Adresse de livraison
                                        </figcaption>
                                        <div class="ps-block__content">
                                            <p>
                                                Vous n'avez pas encore fourni votre adresse de livraison.
                                            </p>
                                            <nuxt-link
                                                to="/account/edit-address"
                                            >
                                                <!--<a>Edit</a>-->
                                            <button
                                                style="padding: 10px; margin-bottom: 0;"
                                                type="submit"
                                                class="ps-btn ps-btn--fullwidth"
                                                @click.prevent="handleSubmit"
                                            >
                                                Modifier
                                            </button>
                                            </nuxt-link>
                                        </div>
                                    </figure>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import AccountLinks from './modules/AccountLinks';
export default {
    name: 'Addresses',
    components: { AccountLinks },
    data() {
        return {
            accountLinks: [
                {
                    text: 'Informations sur votre compte',
                    url: '/account/user-information',
                    icon: 'icon-user'
                },
                {
                    text: 'Notifications',
                    url: '/account/notifications',
                    icon: 'icon-alarm-ringing'
                },
                {
                    text: 'Factures',
                    url: '/account/invoices',
                    icon: 'icon-papers'
                },
                {
                    text: 'Adresses',
                    url: '/account/addresses',
                    icon: 'icon-map-marker',
                    active: true
                },
                {
                    text: 'Produits récemment consultés',
                    url: '/account/recent-viewed-product',
                    icon: 'icon-store'
                },
                {
                    text: 'Liste de souhaits',
                    url: '/account/wishlist',
                    icon: 'icon-heart'
                }
            ]
        };
    }
};
</script>

<style lang="scss" scoped></style>
