<template>
  <body style="background-color: #DFDFDF">
    <h1 class="font-black mb-3">Contact</h1>
    <p>
      Email: {{ contact.Email1 }} <br />
      Email: {{ contact.Email2 }} <br />
      Tel: {{ contact.Tel }} <br />
      Facebook: {{ contact.Facebook }} <br />
      Line: {{ contact.Line }}
    </p>
    <button @click="goToHome()">
      <img
        src="data:image/png;base64,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"
        width="150"
      />
    </button>
  </body>
</template>
<style>
h1 {
  text-align: center;
  font-size: 70px;
}
p {
  text-align: center;
  font-size: 40px;
}
div {
  text-align: center;
}
</style>
<script>
export default {
  data: () => ({
    contact: {
      Email1: "off0891573693@gmail.com",
      Email2: "bh.intouch_st@tni.ac.th",
      Tel: "0814309650",
      Facebook: "OFF Tipparat",
      Line: "off0891573693",
    },
  }),
  methods: {
    goToHome() {
      this.$router.push("/");
    },
  },
};
</script>