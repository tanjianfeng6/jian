<template>
    <div class="login">
       <h1>后台管理</h1>
       <el-form :label-position="left" label-width="80px" :model="formLabelAlign">
            <el-form-item label="账号">
                <el-input v-model="formLabelAlign.name"></el-input>
            </el-form-item>
            <el-form-item label="密码">
                <el-input v-model="formLabelAlign.type"></el-input>
            </el-form-item>
        </el-form>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                a:10,
                b:20
            }
        },

        //组件初始化完毕，自动调用
        create() {
            //测试
            this.$http.get(this.$api.islogin).then(res => {
                console.log(res.data);
            });
        }
    }
</script>

<style scoped>

</style>