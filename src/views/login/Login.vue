<template>
    <div class="Login">
        <div class="container-fluid">
            <div class="row">
                <div class="col-12 col-sm-6 col-lg-4 login-fields-section">
                    <LoginFields></LoginFields>
                </div>
                <div class="col-sm-6 col-lg-8 splash-area d-none d-sm-block ">
                    <div class="overlay"></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';
    import LoginFields from '@/components/login/LoginFields.vue';

    @Component({
        components: {LoginFields},
    })
    export default class Login extends Vue {

    }

</script>

<style type="scss" scoped>

    .login-fields-section {
        min-height: 100vh;
        /*background: #f9f9f9;*/

        display: flex;
        align-items: center;
        justify-items: center;

        width: 100%;
        padding: 40px;
    }

    .overlay {
        background-color: #588eff;
        position: relative;
        width: 100%;
        height: 100%;
        filter: contrast(1.75);
        opacity: 0.5;
        z-index: 2;
    }

    .splash-area {
        background: url("../../assets/icebergs.jpg");
        background-size: cover;
        background-repeat: no-repeat;
        background-position: right top;
        padding: 0;
    }

</style>