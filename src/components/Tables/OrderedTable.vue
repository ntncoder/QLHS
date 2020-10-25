<template>
  <div>
    <md-table v-model="users" :table-header-color="tableHeaderColor">
      <md-table-row slot="md-table-row" slot-scope="{ item }" v-on:dblclick="selectRow()">
        <md-table-cell md-label="ID">{{ item.id }}</md-table-cell>
        <md-table-cell md-label="Tên">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="Lớp">{{ item.class }}</md-table-cell>
        <md-table-cell md-label="Nơi ở">{{ item.address }}</md-table-cell>
        <md-table-cell md-label="">
          <md-button class="md-primary" v-on:click="edit()">Sửa</md-button>
          <md-button class="md-accent" v-on:click="deleteStudent()">Xóa</md-button>
        </md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "ordered-table",
  props: {
    tableHeaderColor: {
      type: String,
      default: ""
    }
  },
  data() {
    return {
      selected: [],
      users: [
        {
          id: 1,
          name: "Nguyễn Ngọc Linh",
          class: "11A1",
          address: "Ứng Hòa - Cầu Giấy",
        },
        {
          id: 2,
          name: "Nguyễn Hòa Anh",
          class: "11A1",
          address: "Ứng Hòa - Cầu Giấy",
        },
                {
          id: 3,
          name: "Nguyễn Minh Trí",
          class: "11A1",
          address: "Ứng Hòa - Cầu Giấy",
        },
        
      ]
    };
  },
  methods: {
    //
    edit() {
      console.log("Sửa");
    },

    //
    deleteStudent() {
      console.log("Xóa");
    },
    //
    selectRow(){
      console.log("Click row")
    }
  }
};
</script>
