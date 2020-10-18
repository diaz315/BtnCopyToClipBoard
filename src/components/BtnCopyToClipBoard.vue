<template>
    <a href="javascript:void(0)" v-on:click="copytoclipboard(value)" :title="'Copiar '+propertyname+' : '+value">
        <button>{{titlebutton}}</button>
    </a>
</template>

<script>
    import Vue from 'vue'
    import Clipboard from 'v-clipboard'

    Vue.use(Clipboard)

    export default {
        name: "BtnCopyToClipBoard",
        components: {
            
        }, props: {
            propertyname: String,
            titlebutton: String,
            value: [String, Number]
        },
        data() {
            return {

            };
        }, methods: {
            copytoclipboard: function (value) {
                this.$clipboard(value)
            }
        }
    };
</script>

<style>
  /*@import '../assets/fontawesome/js/fontawesome.min.js';*/
</style>