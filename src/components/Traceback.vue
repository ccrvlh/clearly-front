<template>
  <div>
    <el-dialog
    title="Tips"
    :visible.sync="dialogVisible"
    width="30%">
        <code>
        Traceback (most recent call last):
            File "/path/to/example.py", line 4, in <module>
                greet('Chad')
            File "/path/to/example.py", line 2, in greet
                print('Hello, ' + someon)
            NameError: name 'someon' is not defined
        </code>
    </el-dialog>
  </div>
</template>

<script>
export default {
    name: 'Traceback',
    props: {
        dialogVisible: Boolean
    }
}
</script>

<style>

</style>