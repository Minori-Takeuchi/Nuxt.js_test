<template>
  <div class="management">
    <table>
      <tr class="w">
        <th class="w">名前</th>
        <th>ID</th>
      </tr>
      <tr v-for="student in students" :key="student.id" class="w">
        <td>{{ student.name }}</td>
        <td>{{ student.id }}</td>
      </tr>
    </table><br>
    <nuxt-link to="/" class="m-50">戻る</nuxt-link>
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
  methods: {
    
  }
};
</script>


<style>
.management {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  text-decoration: dotted;
  flex-wrap: wrap;
  width: 300px;
}
.w {
  width: 100px;
  margin: 100px;
}
.m-50 {
  margin-bottom: 100px;
}
</style>