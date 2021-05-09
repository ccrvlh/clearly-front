<template>
  <div class="all__information">
    <div class="content">
      <br>
      <h3 style="float: left">Database</h3>
      <br>

        <el-form ref="form" :model="form" label-width="120px">
          
          <br>
          
          <el-form-item label="Maximum Tasks">
            <el-input v-model="form.name"></el-input>
          </el-form-item>

          <el-form-item label="Ignore Workers">
            <el-input v-model="form.name"></el-input>
          </el-form-item>

          <el-form-item label="Ignore Queues">
            <el-input v-model="form.name"></el-input>
          </el-form-item>

          <el-form-item label="Time Window">
            <el-input v-model="form.name"></el-input>
          </el-form-item>
          
        </el-form>
      <br>
      <br>  
      <h3 style="float: left">Visualization</h3>
      <br>

      <el-form>
        <br>


          
          <el-form-item label="Instant delivery">
            <span style="float:left">
            <el-switch v-model="form.delivery"></el-switch>
            </span>
          </el-form-item>
          
          <el-form-item label="Activity type">
            <el-checkbox-group v-model="form.type">
              <el-checkbox label="Online activities" name="type"></el-checkbox>
              <el-checkbox label="Promotion activities" name="type"></el-checkbox>
              <el-checkbox label="Offline activities" name="type"></el-checkbox>
              <el-checkbox label="Simple brand exposure" name="type"></el-checkbox>
            </el-checkbox-group>
          </el-form-item>
          
          <el-form-item label="Resources">
            <el-radio-group v-model="form.resource">
              <el-radio label="Sponsor"></el-radio>
              <el-radio label="Venue"></el-radio>
            </el-radio-group>
          </el-form-item>
          
          <el-form-item label="Activity form">
            <el-input type="textarea" v-model="form.desc"></el-input>
          </el-form-item>
          
          <span style="float: right">
          <el-form-item>
            <el-button type="primary" @click="onSubmit">Create</el-button>
            <el-button>Cancel</el-button>
          </el-form-item> 
          </span>
        </el-form>

    </div>

  </div>
</template>

<script>
export default {
    name: 'Content',
    data() {
      return {
        form: {
          name: '',
          region: '',
          date1: '',
          date2: '',
          delivery: false,
          type: [],
          resource: '',
          desc: ''
        }
      }
    }    
}
</script>

<style scoped>

.all__information {
  width: 100%;
  height: 100%;
  border:grey;
  border-width: 10px;
  background: white;
  position:relative;;
  box-shadow: grey;
}

.content {
  margin-left: 20%;
  margin-right: 20%;
  float: left;
}

</style>