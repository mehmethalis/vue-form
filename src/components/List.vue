<template>
  <table class="table">
    <tr class="table-header">
      <th class="t-head" align="left" v-for="title in columns">
        {{ title }}
      </th>
    </tr>
    <tr class="t-row" v-for="entry in rows" :key="entry.id">
      <td class="t-cell" v-for="cell in Object.values(entry)" :key="cell">{{ cell }}</td>
    </tr>
  </table>
</template>

<script>
export default {
  name: "List",
  props: {
    columns: Array,
    rows: Array,
  },
  data() {
    return {};
  },
};
</script>

<style>
.table {
  text-align: start;
}

.t-head {
  color: #6f7189;
  background: #f1f2ff;

  padding: 10px 15px;
}

.t-cell {
  padding: 10px 15px;
}

.t-row {
  border: 1px solid #6f7189;
  transition: all ease-in-out 0.2s;
}
.t-row:hover {
  background-color: rgba(0, 0, 0, 0.05);
}
</style>
