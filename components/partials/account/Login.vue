<template lang="html">
    <form>
        <div class="ps-form__content">
            <h5>Connectez-vous à votre compte</h5>
            <div class="form-group">
                <v-text-field
                    v-model="username"
                    class="ps-text-field"
                    :error-messages="usernameErrors"
                    @input="$v.username.$touch()"
                    placeholder="Nom d'utilisateur ou e-mail"
                    height="50"
                    outlined
                />
            </div>
            <div class="form-group">
                <v-text-field
                    v-model="password"
                    type="password"
                    class="ps-text-field"
                    :error-messages="passwordErrors"
                    @input="$v.password.$touch()"
                    placeholder="Mot de passe"
                    height="50"
                    outlined
                />
            </div>
            <div class="form-group">
                <v-checkbox label="Se souvenir de moi" color="warning" />
            </div>
            <div class="form-group submit">
                <button
                    style="padding: 10px"
                    type="submit"
                    class="ps-btn ps-btn--fullwidth"
                    @click.prevent="handleSubmit"
                >
                    S'identifier
                </button>
            </div>
        </div>
        <!--<div class="ps-form__footer">
            <p>Se connecter avec : </p>
            <ul class="ps-list--social">
                <li>
                    <a href="#" class="facebook">
                        <i class="fa fa-facebook"></i>
                    </a>
                </li>
                <li>
                    <a href="#" class="google">
                        <i class="fa fa-google-plus"></i>
                    </a>
                </li>
                <li>
                    <a href="#" class="twitter">
                        <i class="fa fa-twitter"></i>
                    </a>
                </li>
                <li>
                    <a href="#" class="instagram">
                        <i class="fa fa-instagram"></i>
                    </a>
                </li>
            </ul>
        </div>-->
    </form>
</template>

<script>
import { email, required } from 'vuelidate/lib/validators';
import { validationMixin } from 'vuelidate';

export default {
    name: 'Login',
    computed: {
        usernameErrors() {
            const errors = [];
            if (!this.$v.username.$dirty) return errors;
            !this.$v.username.required && errors.push('This field is required');
            return errors;
        },
        passwordErrors() {
            const errors = [];
            if (!this.$v.password.$dirty) return errors;
            !this.$v.password.required && errors.push('This field is required');
            return errors;
        }
    },
    data() {
        return {
            username: null,
            password: null
        };
    },
    validations: {
        username: { required },
        password: { required }
    },
    methods: {
        handleSubmit() {
            this.$v.$touch();
            if (!this.$v.$invalid) {
                this.$store.dispatch('auth/setAuthStatus', true);
                this.$router.push('/');
            }
        }
    }
};
</script>

<style lang="scss" scoped></style>
