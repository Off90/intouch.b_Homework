<template>
  <body style="background-color: #DFDFDF">
    <h1 class="font-black mb-3">Portfolio</h1>
    <img src="@/assets/getstudentimage.jpg" width="200" height="250" />
    <p>
      ชื่อ: {{ portfolio.f_name }} <br />
      นามสกุล: {{ portfolio.l_name }} <br />
      ชื่อเล่น: {{ portfolio.n_name }} <br />
      อายุ: {{ portfolio.age }} ปี<br />
      ความสามารถ: {{ portfolio.skill }} <br />
      {{ portfolio.soft_skill }} <br />
      ภาษาที่เขียนเป็น: {{ portfolio.code }} <br />
    </p>
    <p>
      Contact Here:
      <button @click="goToContact()">
        <img
          src="https://iconarchive.com/download/i85562/graphicloads/100-flat/contact.ico"
          width="100"
        />
      </button>
    </p>
  </body>
</template>
<style>
h1 {
  text-align: center;
}
p {
  text-align: center;
  font-size: 30px;
}
div {
  text-align: center;
}
</style>

<script>
export default {
  data: () => ({
    portfolio: {
      f_name: "นาย อินทัช",
      l_name: "พันธุพงษ์",
      n_name: "อ๊อฟ",
      age: 20,
      skill: "สามารถใช้ Microsoft Office ได้ดี เขียนโค้ดได้",
      soft_skill:
        "สามารถเรียนรู้ได้เร็ว,เปิดรับสิ่งใหม่ๆเสมอ,พร้อมรับคำวิจารณ์และพร้อมปรับปรุง,รับต่อแรงกดดันได้",
      code: "C,C++,Python,SQL/PLSQL,Java,JavaScript,Html",
    },
  }),
  methods: {
    goToContact() {
      this.$router.push("/contact");
    },
  },
};
</script> 
