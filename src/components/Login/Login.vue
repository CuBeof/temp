<template>
    <div class="wrapper mini-box">
        <v-card>
            <LoginHeader/>
            <LoginSectionTitle>Đăng nhập / Đăng ký tự động bằng</LoginSectionTitle>
            <LoginWithSocial/>
            <LoginSectionTitle>Hoặc sử dụng e-mail</LoginSectionTitle>
            <LoginForm/>
        </v-card>
    </div>
</template>

<script>
import LoginHeader from './LoginHeader'
import LoginWithSocial from './LoginWithSocial'
import LoginForm from './LoginForm'
import LoginSectionTitle from './LoginSectionTitle'

export default {
  components: {
    LoginHeader,
    LoginWithSocial,
    LoginForm,
    LoginSectionTitle
  }
}
</script>
<style scoped>
.wrapper {
    margin-left: auto;
    margin-right: auto;
    padding-top: 2rem;
    padding-bottom: 2rem;
    position: relative;
    z-index: 1;
}
.mini-box {
	max-width: 420px;
	width: 100%
}
</style>