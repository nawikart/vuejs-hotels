<template>
  <div style="margin-top: 100px;">
        <penerima :datadariroot="datadariroot"/>
        <pengirim @clickedx="onClickChild"/>
  </div>
</template>


<script>
import Pengirim from '~/components/pengirim.vue'
import Penerima from '~/components/penerima.vue'

export default {
  components: {
    Penerima,
    Pengirim
  },

   data() {
    return {
      datadariroot:''
    }
  },

  methods: {
    onClickChild (value) {
     this.datadariroot = value //ini ngeproses dijadiin variabel biar siap kirim ke komponen PENERIMA
    }
  }
}
</script>