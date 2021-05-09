<template>
    <div>
      <el-dialog
        title="Tips"
        :visible.sync="dialogVisible"
        width="50%"
        :before-close="handleClose"
        :modalAppendToBody="false">

        <TaskDetails />
        
        <span slot="footer" class="dialog-footer">
          <el-button @click="dialogVisible = false">Cancel</el-button>
          <el-button type="primary" @click="dialogVisible = false">Confirm</el-button>
        </span>
      </el-dialog>

        <span style="float: left; margin-bottom: 10px">
          <span style="padding: 5px;"><el-select placeholder="Workers" value="Filter workers..."></el-select></span>
          <span style="padding: 5px;"><el-select placeholder="State" value="Filter status..."></el-select></span>
          <span style="padding: 5px;"><el-select placeholder="Task Name" value="Filter name..."></el-select></span>
        </span>
        <span style="float: right; margin-bottom: 10px">
          <span style="padding: 10px;">
            Hide successful tasks<el-switch v-model="hideSuccess"></el-switch>
          </span>
          <span style="padding: 5px;">    <el-date-picker
            v-model="value2"
            type="datetimerange"
            :picker-options="pickerOptions"
            range-separator="To"
            start-placeholder="Start date"
            end-placeholder="End date"
            align="right">
          </el-date-picker></span>
        </span>
  <el-table
    ref="filterTable"
    :data="tableData.filter(data => !search || data.state.toLowerCase().includes(search.toLowerCase()))"
    style="width: 100%">
    <el-table-column
    sortable
    :filter-method="filterHandler"
      label="Date"
      prop="date">
    </el-table-column>
    <el-table-column
        sortable
        :filter-method="filterHandler"
      label="Worker"
      prop="worker">
    </el-table-column>
    <el-table-column
    sortable
    :filter-method="filterHandler"
      label="Task"
      prop="task">
    </el-table-column>
    <el-table-column
    sortable
    :filter-method="filterHandler"
      label="State"
      prop="State">
      <template slot-scope="scope">
        <el-tag effect="dark" size="medium" @click='tracebackDialog = true' :type='scope.row.taskStatusType'>{{ scope.row.state }}</el-tag>   
      </template>
    </el-table-column>
    <el-table-column
    sortable
    :filter-method="filterHandler"
      label="Result"
      prop="result">
    </el-table-column>
    <el-table-column
    sortable
    :filter-method="filterHandler"
      label="Started"
      prop="started">
    </el-table-column>
    <el-table-column
    sortable
    :filters="[]"
    :filter-method="filterHandler"
      label="Finished"
      prop="finished">
    </el-table-column>
    <el-table-column
    sortable
    :filter-method="filterHandler"
    filter-placement="bottom-end"
      label="Ellapsed"
      prop="ellapsed">
    </el-table-column>
    <el-table-column
      align="right">
      <template slot="header">
        <el-input
          v-model="search"
          size="mini"
          placeholder="Type to search"/>
      </template>
      <template slot-scope="scope">
        <el-button
          size="mini"
          @click="openTaskDetails(scope.$index, scope.row)">Details</el-button>
      </template>
    </el-table-column>
    
  </el-table>
  <el-pagination
  layout="prev, pager, next"
  :total="100">
</el-pagination>




    </div>  
</template>

<script>
import TaskDetails from '@/components/TaskDetails'

  export default {
    components: {TaskDetails},
    data() {
      return {
        dialogVisible: false,
        taskStatusType: null,
        tableData: [{
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Success',
          result: 'None',
          taskStatusType: 'success'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Success',
          result: 'None',
          taskStatusType: 'success'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Success',
          result: 'None',
          taskStatusType: 'success'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Success',
          result: 'None',
          taskStatusType: 'success'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Success',
          result: 'None',
          taskStatusType: 'success'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Failed',
          result: 'None',
          taskStatusType: 'danger'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Success',
          result: 'None',
          taskStatusType: 'success'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Running',
          result: 'None',
          taskStatusType: 'info'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Running',
          result: 'None',
          taskStatusType: 'info'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Success',
          result: 'None',
          taskStatusType: 'success'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Success',
          result: 'None',
          taskStatusType: 'success'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Running',
          result: 'None',
          taskStatusType: 'info'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Running',
          result: 'None',
          taskStatusType: 'info'
        }, {
          date: '18h23m20s Apr/04/20',
          worker: 'celery@aws-34239-sdn-93',
          task: 'app.tasks.long_task',
          started: '2016-05-03',
          finished: '2016-05-03',
          ellapsed: '2016-05-03',
          address: 'No. 189, Grove St, Los Angeles',
          state: 'Running',
          result: 'None',
          taskStatusType: 'info'
        }],
        pickerOptions: {
          shortcuts: [{
            text: 'Last week',
            onClick(picker) {
              const end = new Date();
              const start = new Date();
              start.setTime(start.getTime() - 3600 * 1000 * 24 * 7);
              picker.$emit('pick', [start, end]);
            }
          }, {
            text: 'Last month',
            onClick(picker) {
              const end = new Date();
              const start = new Date();
              start.setTime(start.getTime() - 3600 * 1000 * 24 * 30);
              picker.$emit('pick', [start, end]);
            }
          }, {
            text: 'Last 3 months',
            onClick(picker) {
              const end = new Date();
              const start = new Date();
              start.setTime(start.getTime() - 3600 * 1000 * 24 * 90);
              picker.$emit('pick', [start, end]);
            }
          }]
        },
        search: '',
        value1: [new Date(2000, 10, 10, 10, 10), new Date(2000, 10, 11, 10, 10)],
        value2: '' ,
        hideSuccess: null      
      }
    },
    methods: {
      handleEdit(index, row) {
        console.log(index, row);
      },
      handleDelete(index, row) {
        console.log(index, row);
      },
      printScope(scope) {
          console.log(scope)
          console.log(this.scope)
      },
      filterHandler(value, row, column) {
        const property = column['property'];
        return row[property] === value;
      },
      openTaskDetails(index, row) {
        this.dialogVisible = true
        console.log(index, row)
      },
      handleClose(done) {
        console.log(done)
      }
    }
  }
</script>