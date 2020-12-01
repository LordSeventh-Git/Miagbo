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
                        <div class="ps-section__header">
                            <h3>
                                Facture #500884010 -
                                <strong>Livraison réussie</strong>
                            </h3>
                        </div>
                        <div class="ps-section__content">
                            <div class="row">
                                <div class="col-md-4 col-12">
                                    <figure class="ps-block--invoice">
                                        <figcaption>
                                            Adresse
                                        </figcaption>
                                        <div class="ps-block__content">
                                            <strong>
                                                John Walker
                                            </strong>
                                            <p>
                                                Address: 3481 Poe Lane,
                                                Westphalia, Kansas
                                            </p>
                                            <p>
                                                Phone: 913-489-1853
                                            </p>
                                        </div>
                                    </figure>
                                </div>
                                <div class="col-md-4 col-12">
                                    <figure class="ps-block--invoice">
                                        <figcaption>                                            
                                            Frais d'expédition
                                        </figcaption>
                                        <div class="ps-block__content">
                                            <p>
                                                Frais d'expédition : gratuit
                                            </p>
                                        </div>
                                    </figure>
                                </div>
                                <div class="col-md-4 col-12">
                                    <figure class="ps-block--invoice">
                                        <figcaption>
                                            Paiement
                                        </figcaption>
                                        <div class="ps-block__content">
                                            <p>
                                                Méthode de paiment : Visa
                                            </p>
                                        </div>
                                    </figure>
                                </div>
                            </div>
                            <div class="table-responsive">
                                <TableInvoice :products="invoiceProducts" />
                            </div>
                            <nuxt-link to="/account/invoices">
                                <a class="ps-btn ps-btn--sm ">
                                    Retour aux factures
                                </a>
                            </nuxt-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import AccountLinks from './modules/AccountLinks';
import TableInvoice from './modules/TableInvoice';
export default {
    name: 'InvoiceDetail',
    components: { TableInvoice, AccountLinks },
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
                    icon: 'icon-papers',
                    active: true
                },
                {
                    text: 'Adresses',
                    url: '/account/addresses',
                    icon: 'icon-map-marker',
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
            ],
            invoiceProducts: [
                {
                    id: '6',
                    thumbnail: '/img/products/shop/5.jpg',
                    title: 'Grand Slam Indoor Of Show Jumping Novel',
                    vendor: "Robert's Store",
                    sale: true,
                    price: '32.99',
                    sale_price: '41.00',
                    rating: true,
                    ratingCount: '4',
                    badge: [
                        {
                            type: 'sale',
                            value: '-37%'
                        }
                    ]
                },
                {
                    id: '7',
                    thumbnail: '/img/products/shop/6.jpg',
                    title: 'Sound Intone I65 Earphone White Version',
                    vendor: 'Youngshop',
                    sale: true,
                    price: '100.99',
                    sale_price: '106.00',
                    rating: true,
                    ratingCount: '5',
                    badge: [
                        {
                            type: 'sale',
                            value: '-5%'
                        }
                    ]
                }
            ]
        };
    }
};
</script>

<style lang="scss" scoped></style>
