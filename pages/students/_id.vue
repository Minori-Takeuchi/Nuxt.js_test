<template>
  <div class="student_id">
    <h1 class="name">{{ student.name }}</h1>
      <nuxt-link to="/students" class="link">生徒一覧へ戻る</nuxt-link>
      <div class="link">|</div>
      <nuxt-link to="/" class="link">トップページへ</nuxt-link>
  </div>
</template>


<script>
export default {
  validate({ params }) {
    if (params.id == undefined) {
      return false
    } else {
      return true
    }
  },
  data() {
    return {
      students: [
        {
          id: "qnfungqxllc3m1ak",
          name: "生徒A",
        },
        {
          id: "7j9cumkgsq6l264c",
          name: "生徒B",
        },
        {
          id: "eo34bhey9m0d92ou",
          name: "生徒C",
        },
      ],
      student: {}
    };
  },
  methods: {
  getData() {
    this.students.forEach((student) => {
      if (student.id === this.$route.params.id) {
        this.student = student
      }
    })
    },
  },
  created() {
    this.getData()
  }
}
</script>


<style>
.student_id {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-wrap: wrap;
}
.name {
  margin-top:200px;
  width: 100%;
}
.link{
  margin-right: 5px;
  margin-bottom: 200px;
}
</style>