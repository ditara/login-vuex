<template>
    <div class="container">
        <div class = "form_dropdown">
            <h2>Login</h2>
        <div class="form-group">
            <label for="exampleInputEmail1">Username</label>
            <input type="text" class="form-control" name="username" v-model="input.username" placeholder="Username" />
            <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
        </div>
        <div class="form-group">
            <label for="exampleInputPassword1">Password</label>
            <input type="password" class="form-control" name="password" v-model="input.password" placeholder="Password" />
        </div>
        <button type="button" class="btn btn-success" v-on:click="login()">Login</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Login',
        data() {
            return {
                input: {
                    username: "",
                    password: ""
                }
            }
        },
        methods: {
            login() {
                if(this.input.username != "" && this.input.password != "") {
                    if(this.input.username == this.$parent.mockAccount.username && this.input.password == this.$parent.mockAccount.password) {
                        this.$emit("authenticated", true);
                        this.$router.replace({ name: "Secure" });
                    } else {
                        console.log("The username and / or password is incorrect");
                    }
                } else {
                    console.log("A username and password must be present");
                }
            }
        }
    }
</script>

<style scoped>

    .container {
  max-width: 700px;
  margin: 0 auto;
}
.form_dropdown {
  padding: 20px;
  width: 400px;
  margin: 0 auto;
  margin-bottom: 10px;
  margin-top: 60px;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  border-radius: 5px;
  text-align: center;
  background-color: #fffdea
}
h2 {
  color: #b9a700;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif
}
</style>