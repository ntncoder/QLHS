<template>
  <div>
    <md-table
      v-model="classStudent"
      :table-header-color="tableHeaderColor"
      v-show="mode == 1"
    >
      <md-table-toolbar class="md-layout">
        <div class="md-layout-item md-small-size-100 md-size-50">
          <md-autocomplete
            class="search"
            v-model="selectedEmployee"
            :md-options="employees"
          >
            <label>Search...</label>
          </md-autocomplete>
        </div>
      </md-table-toolbar>
      <md-table-row
        slot="md-table-row"
        slot-scope="{ item }"
        v-on:dblclick="selectRow()"
      >
        <md-table-cell md-label="">
          <md-card>
            <md-card-header>
              <div class="md-title">{{ item.name }}</div>
            </md-card-header>

            <md-card-content> GVCN: {{ item.monitor }} </md-card-content>

            <md-card-actions>
              <md-button>Cập nhật điểm</md-button>
              <md-button>Chỉnh sửa</md-button>
              <md-button>thời khóa biếu</md-button>
            </md-card-actions>
          </md-card>
        </md-table-cell>
      </md-table-row>
    </md-table>

    <div>
      <md-dialog :md-active.sync="active" class="student-detail">
        <md-dialog-title>Học sinh</md-dialog-title>
        <div class="ms-layout" style="display: flex">
          <div class="md-layout-item md-small-size-100 md-size-40">
            <md-avatar class="avatar">
              <img src="\src\assets\img\side-bar-2.jpg" alt="People" />
            </md-avatar>
          </div>

          <md-field class="md-layout-item md-small-size-100 md-size-60">
            <label>Họ và tên</label>
            <md-input v-model="regular" md-counter="50"></md-input>
          </md-field>
        </div>
        <md-field>
          <label>Địa chỉ thường trú</label>
          <md-input v-model="regular"></md-input>
        </md-field>
        <div class="md-layout">
          <div class="md-layout-item md-small-size-100 md-size-50">
            <md-datepicker v-model="selectedDate">
              <label>Ngày sinh</label>
            </md-datepicker>
          </div>
          <div class="md-layout-item md-small-size-100 md-size-50">
            <md-field>
              <label>Lớp</label>
              <md-input v-model="regular"></md-input>
            </md-field>
          </div>
        </div>
        <div class="md-layout" style="display: flex">
          <div class="md-layout-item md-small-size-100 md-size-50">
            <md-field>
              <label>Giới tính</label>
              <md-input v-model="regular"></md-input>
            </md-field>
          </div>
          <div class="md-layout-item md-small-size-100 md-size-50">
            <md-field>
              <label>Dân tộc</label>
              <md-input v-model="regular"></md-input>
            </md-field>
          </div>
        </div>
        <div class="md-layout" style="display: flex">
          <div class="md-layout-item md-small-size-100 md-size-60">
            <md-field>
              <label>Họ tên bố</label>
              <md-input v-model="regular"></md-input>
            </md-field>
          </div>
          <div class="md-layout-item md-small-size-100 md-size-40">
            <md-field>
              <label>Liên hệ</label>
              <md-input v-model="regular"></md-input>
            </md-field>
          </div>
        </div>
        <div class="md-layout" style="display: flex">
          <div class="md-layout-item md-small-size-100 md-size-60">
            <md-field>
              <label>Họ tên mẹ</label>
              <md-input v-model="regular"></md-input>
            </md-field>
          </div>
          <div class="md-layout-item md-small-size-100 md-size-40">
            <md-field>
              <label>Liên hệ</label>
              <md-input v-model="regular"></md-input>
            </md-field>
            <md-button class="md-raised" v-on:click="cancelEdit()"
              >Hủy bỏ</md-button
            >
            <md-button class="md-primary" v-on:click="editStudent()"
              >Đồng ý</md-button
            >
          </div>
        </div>
      </md-dialog>
    </div>
  </div>
</template>

<script>
export default {
  name: "class-list",

  data() {
    return {
      mode: 1,
      active: false,
      selected: [],
      selectedEmployee: null,
      employees: [
        "Jim Halpert",
        "Dwight Schrute",
        "Michael Scott",
        "Pam Beesly",
        "Angela Martin",
        "Kelly Kapoor",
        "Ryan Howard",
        "Kevin Malone"
      ],
      users: [
        {
          id: 1,
          name: "Nguyễn Ngọc Linh",
          class: "11A1",
          address: "Ứng Hòa - Cầu Giấy"
        },
        {
          id: 2,
          name: "Nguyễn Hòa Anh",
          class: "11A1",
          address: "Ứng Hòa - Cầu Giấy"
        },
        {
          id: 3,
          name: "Nguyễn Minh Trí",
          class: "11A1",
          address: "Ứng Hòa - Cầu Giấy"
        }
      ],
      classStudent: [
        {
          id: 1,
          name: "10A1",
          monitor: "Hoàng Khánh Huyền",
          numberStudent: "31"
        },
        {
          id: 2,
          name: "10A2",
          monitor: "Đỗ Lâm Anh",
          numberStudent: "31"
        },
        {
          id: 3,
          name: "10A3",
          monitor: "Nguyễn Thị Vui",
          numberStudent: "31"
        },
        {
          id: 1,
          name: "10A4",
          monitor: "Phạm Thu Hà",
          numberStudent: "31"
        }
      ]
    };
  },
  methods: {
    //
    edit() {
      console.log("Sửa");
      this.active = true;
    },

    //
    deleteStudent() {
      console.log("Xóa");
    },
    //
    selectRow() {
      console.log("Click row");
    }
  }
};
</script>
<style scoped>
.student-detail {
  height: 800px;
  width: 700px;
  padding: 20px;
}
.avatar {
  width: 80px;
  height: 80px;
  background-color: aquamarine;
}
</style>
