<template>
    <div id="TenantChanger">
        <div class="row">
            <div class="col">
                <p>Current Tenant: <span>touch</span> Change Tenant</p>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    import {Component, Prop, Vue} from 'vue-property-decorator';


    @Component({
        components: {},
    })
    export default class TenantChanger extends Vue {

        @Prop() public tenantModalEvent: any;

        public emitModalEvent(): void {
            this.tenantModalEvent();
        }

    }

</script>

<style lang="scss">

    #TenantChanger {
        margin-top: 150px;

        p {
            font-size: 10px;

            span {
                font-size: 30px;
            }
        }
    }


</style>