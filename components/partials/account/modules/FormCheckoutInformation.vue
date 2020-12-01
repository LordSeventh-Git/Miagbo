<template lang="html">
    <div class="ps-form__billing-info">
        <h3 class="ps-form__heading">
            Informations de contact
        </h3>
        <div class="form-group">
            <label>E-mail ou numéro de téléphone <sup>*</sup></label>
            <v-text-field
                placeholder="E-mail ou numéro de téléphone"
                outlined
                height="50"
            />
        </div>
        <div class="form-group">
            <v-checkbox
                color="success"
                label="Me tenir informé des offres exclusives ?"
            />
        </div>
        <h3 class="ps-form__heading">
            Adresse de livraison
        </h3>
        <div class="row">
            <div class="col-sm-6">
                <div class="form-group">
                    <label>Prénoms</label>
                    <v-text-field
                        placeholder="Prénoms"
                        outlined
                        height="50"
                    />
                </div>
            </div>
            <div class="col-sm-6">
                <div class="form-group">
                    <label>Nom</label>
                    <v-text-field
                        placeholder="Nom"
                        outlined
                        height="50"
                    />
                </div>
            </div>
        </div>
        <div class="form-group">
            <label>Adresse</label>
            <v-text-field placeholder="Adresse" outlined height="50" />
        </div>
        <div class="form-group">
            <label>Appartement</label>
            <v-text-field
                placeholder="Appartement, suite, etc. (optionnel)"
                outlined
                height="50"
            />
        </div>
        <div class="row">
            <div class="col-sm-6">
                <div class="form-group">
                    <label>Ville</label>
                    <v-text-field placeholder="Ville" outlined height="50" />
                </div>
            </div>
            <div class="col-sm-6">
                <div class="form-group">
                    <label>Code postal</label>
                    <v-text-field
                        placeholder="Code postal"
                        outlined
                        height="50"
                    />
                </div>
            </div>
        </div>
        <div class="form-group">
            <v-checkbox
                color="success"
                label="Enregistrez ces informations pour la prochaine fois"
            />
        </div>
        <div class="ps-form__submit">
            <nuxt-link to="/account/shopping-cart">
                <i class="icon-arrow-left mr-1"></i>
                Retourner au panier
            </nuxt-link>
            <div class="ps-block__footer">
                <button class="ps-btn" @click="handleToShipping" style="padding: 10px;">
                    Continuer à expédier
                </button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FormCheckoutInformation',
    methods: {
        handleToShipping() {
            this.$router.push('/account/shipping');
        }
    }
};
</script>

<style lang="scss" scoped></style>
