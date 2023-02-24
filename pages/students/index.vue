<template>
  <div class="students">
    <h1>生徒一覧</h1>
    <nav>
      <ul>
        <li v-for="student in students" :key="student.id">
        <NuxtLink :to="`/students/${student.id}`" class="student">{{ student.name }}</NuxtLink>
        </li>
      </ul><br>
      <NuxtLink to="/" class="m">戻る</NuxtLink>
    </nav>
  </div>
</template>


<script>
export default {
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
    };
  },
};
</script>


<style>
.students {
  margin: 200px auto;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  width: 200px;
  flex-wrap: wrap;
}
.m {
  margin: 50px;
}

</style>