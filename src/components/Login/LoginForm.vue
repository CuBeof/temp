<template>
    <v-form ref="form" class="pa-6 text-center">
        <v-text-field
        outlined
        clearable
        label="Email"
        type="email"
        prepend-inner-icon="email"
        name="email"
        :rules="[rules.required, rules.email]">
        </v-text-field>
        <v-text-field
        v-model="password"
        outlined label="Mật khẩu"
        prepend-inner-icon="lock"
        :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
        :type="showPassword ? 'text' : 'password'"
        :rules="[rules.required]"
        @click:append="showPassword = !showPassword" name="password">
        </v-text-field>
        <v-btn
        outlined
        x-large
        :loading="isLoading"
        :disabled="isLoading"
        @click="handleLoginButtonClick">
            Login
            <v-icon right>mdi-login</v-icon>
        </v-btn>
    </v-form>
</template>

<script>
export default {
    data: () => ({
        showPassword: false,
        password: '',
        isLoading: false,
        rules: {
            required: value => !!value || 'Chưa nhập mục này.',
            email: value => {
                const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
                return pattern.test(value) || 'Địa chỉ e-mail không hợp lệ.'
            }
        }
    }),
    methods: {
        handleLoginButtonClick() {
            this.isLoading = true
            setTimeout(() => (this.isLoading = false), 3000)
        }
    }
}
</script>

<style scoped>

/* Login Button */
 .custom-loader {
    animation: loader 1s infinite;
    display: flex;
  }
  @-moz-keyframes loader {
    from {
      transform: rotate(0);
    }
    to {
      transform: rotate(360deg);
    }
  }
  @-webkit-keyframes loader {
    from {
      transform: rotate(0);
    }
    to {
      transform: rotate(360deg);
    }
  }
  @-o-keyframes loader {
    from {
      transform: rotate(0);
    }
    to {
      transform: rotate(360deg);
    }
  }
  @keyframes loader {
    from {
      transform: rotate(0);
    }
    to {
      transform: rotate(360deg);
    }
  }
</style>