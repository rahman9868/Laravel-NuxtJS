<template>
    <div class="col-md-6 offset-md-3">
        <div class="card mt-4">
            <div class="card-header">
               
                <p class="mb-0">Login</p>
            </div>
            <div class="card-body">
                <form @submit.prevent="login">
                    <div class="form-group">
                        <label>Email</label>
                        <input v-model="form.email" type="email" class="form-control"  placeholder="Email">
                         
                    </div>
                    <div class="form-group">
                        <label>Password</label>
                        <input v-model="form.password" type="password" class="form-control" placeholder="Password">
                         
                    </div>
                    <div class="form-group">
                        <input type="submit" value="Login" class="btn btn-default w-100">
                    </div>
                </form>
            </div>
        </div>

    </div>

</template>

<script>
export default {
    middleware: 'guest',
    data() {
        return {
            form: {
             
                email: '',
                password: ''
            }
        }
    },
    methods: {
        async login() {
            

            await this.$auth.login({data: this.form});

            this.$router.push(this.$route.query.redirect ? this.$route.query.redirect : '/');
        }

    }
}
</script>