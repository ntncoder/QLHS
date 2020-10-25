<template>
  <div class="content">
    <div
      class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-100"
    >
      <md-card class="md-card-plain">
        <md-card-header data-background-color="green">
          <h4 class="title">Danh sách học sinh {{ className }}</h4>
        </md-card-header>
        <md-card-content>
          <!-- <ordered-table></ordered-table> -->
          <student-list></student-list>
        </md-card-content>
      </md-card>
    </div>
  </div>
</template>

<script>
//import { SimpleTable, OrderedTable } from "@/components";
import StudentList from "./student/student-list.vue";

export default {
  components: {
    //OrderedTable,
    StudentList
  },
  data() {
    return {
      className: ""
    };
  }
};
</script>
