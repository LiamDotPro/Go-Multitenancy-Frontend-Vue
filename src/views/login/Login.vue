<template>
    <div id="Login">
        <div class="container-fluid">
            <div class="row">
                <div class="col-12 col-sm-6 col-lg-4 login-fields-section">
                    <div class="row">
                        <div class="col">
                            <tenant-changer :tenantModalEvent="showModalEvent"></tenant-changer>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col">
                            <LoginFields></LoginFields>
                        </div>
                    </div>
                </div>
                <div class="col-sm-6 col-lg-8 splash-area d-none d-sm-block ">
                    <!--<div class="overlay"></div>-->
                </div>
            </div>
        </div>
        <DefaultModal v-if="showModal" @close="showModal = false"></DefaultModal>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';
    import LoginFields from '@/components/login/LoginFields.vue';
    import TenantChanger from '@/components/login/TenantChanger.vue';
    import DefaultModal from '@/components/shared/DefaultModal.vue';

    @Component({
        components: {DefaultModal, TenantChanger, LoginFields},
    })
    export default class Login extends Vue {

        public showModal: boolean = false;

        public showModalEvent(): void {
            this.showModal = true;
        }

    }

</script>

<style scoped type="scss">

    .login-fields-section {
        min-height: 100vh;
        /*background: #f9f9f9;*/
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
        box-shadow: inset 7px 0 9px -7px rgba(0,0,0,0.4);
    }


    /*Small devices (landscape phones, 576px and up)*/
    @media (min-width: 576px) {
    }

    /*// Medium devices (tablets, 768px and up)*/
    @media (min-width: 768px) {
    }

    /*// Large devices (desktops, 992px and up)*/
    @media (min-width: 992px) {
    }

    /*// Extra large devices (large desktops, 1200px and up)*/
    @media (min-width: 1200px) {
        .login-fields-section {
            padding: 40px 100px;
        }
    }


</style>