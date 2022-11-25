<template>
  <section class="pb-8" id="contact">
    <v-container fluid>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <v-row justify="center">
            <v-col cols="12" sm="5">
              <h1 class="font-weight-light display-1">¿Qué más le gustaría poder calcular?</h1>
              <h3 class="font-weight-light mt-3">
                Dejanos un mensaje con otro cálculo que te gustaría poder hacer.
              </h3>
              <h3 class="font-weight-light mt-3">
                Hecho con amor por Instagram <a href="https://www.instagram.com/soyangiezuniga/">@soyangiezuniga</a> y <a href="https://www.instagram.com/jaibayuelomundial/">@jaibayuelomundial</a>
              </h3>
              <h3 class="font-weight-light mt-3">
                Si quieres contribuir a este proyecto...
              </h3>
              <h3 class="font-weight-light mt-3 mifuente">
                BTC wallet: 1P1MBjBTjRxgtryP4Gaz1D8aY2mAjHQ7QN
              </h3>
              <h3 class="font-weight-light mt-3 mifuente" width="100%">
                BNB BEP20 wallet: 0x7a07D54a7D7dFDd1a808c977fF2D5D3D1c7f2494
              </h3>
              <v-img
              src="@/assets/img/godiamond.png"
              max-width="250px"
              class="mr-4"
              />
              <h3 class="font-weight-light">
               
              </h3>
            </v-col>
            <v-col cols="12" sm="7">
              <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSewapeYZY2tXJyOrK65rD_Zq8vZwsqWsS4y-uCAN6FkVRxiJg/viewform?embedded=true" width="100%" height="418" frameborder="0" marginheight="0" marginwidth="0">Cargando…</iframe>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
    <div class="svg-border-waves text-white">
      <v-img src="~@/assets/img/borderWavesBlue.svg"/>
    </div>
    <v-snackbar
        v-model="snackbar.enabled"
        timeout="3000"
        right
        top
        :color="snackbar.color"
    >
      {{ snackbar.text }}

      <template v-slot:action="{ attrs }">
        <v-btn
            text
            v-bind="attrs"
            @click="snackbar.enabled = false"
        >
          Fechar
        </v-btn>
      </template>
    </v-snackbar>
  </section>
</template>

<style scoped>
#contact {
  background-color: #f4f7f5;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}
.mifuente {
  font-size: 3vw;
}

</style>

<script>
// import {db} from '@/main'

export default {
  data: () => ({
    icons: ["fa-facebook", "fa-twitter", "fa-linkedin", "fa-instagram"],
    valid: true,
    name: "",
    nameRules: [
      (v) => !!v || "O campo nome é obrigatório",
      (v) => (v && v.length >= 6) || "O nome precisa ter mais de 6 caracteres",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "O campo email é obrigatório",
      (v) => /.+@.+\..+/.test(v) || "O E-mail precisa ser válido",
    ],
    textArea: "",
    textAreaRules: [
      (v) => !!v || "O campo de texto é obrigatório",
      (v) => (v && v.length >= 10) || "Mínimo de 10 caracteres",
    ],
    lazy: false,
    snackbar: {
      enabled: false,
      text: '',
      color: ''
    }
  }),
  methods: {
    submit() {
      /*db.collection("contactData").add({
        name: this.name,
        email: this.email,
        message: this.textArea
      }).then(() => {
        this.snackbar.text = "Mensagem enviada com sucesso"
        this.snackbar.color = "success"
        this.snackbar.enabled = true
      }).catch(() => {
        this.snackbar.text = "Erro ao enviar mensagem"
        this.snackbar.color = "danger"
        this.snackbar.enabled = true
      })*/
    }
  }
};
</script>
