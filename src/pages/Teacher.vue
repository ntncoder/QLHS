<template>
  <div class="content">
    <div
      class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-100"
    >
      <md-card class="md-card-plain">
        <md-card-header data-background-color="green">
          <h4 class="title">Danh sách Giáo viên</h4>
        </md-card-header>
        <md-card-content>
          <teacher-list></teacher-list>
        </md-card-content>
      </md-card>
    </div>
  </div>
</template>

<script>
//import { SimpleTable, OrderedTable } from "@/components";
import TeacherList from "./teacher/teacher-list";

export default {
  components: {
    //OrderedTable,
    TeacherList
  },
  data() {
    return {
      className: ""
    };
  }
};
</script>
