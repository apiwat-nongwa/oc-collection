<template>
    <div>
        <StreamBarcodeReader @decode="onDecode" @loaded="onLoaded"></StreamBarcodeReader>
        <hr />

        <span>{{ barcode }}</span>
    </div>
</template>
<script>
import { StreamBarcodeReader } from 'vue-barcode-reader'
export default {
    components: {
        StreamBarcodeReader,
    },
    data() {
        return {
            barcode: null
        }
    },
    methods:{
        onDecode(result){
            // eslint-disable-next-line no-console
            console.log(result);
        },
        onLoaded(){},
    }
}
</script>