<template>
  <section class="login">
    <div class="container">
      <div class="row flex-auto">
        <div class="col-md-12">
          <div class="card login-card">
            <div class="card-body">
              <h1 class="login-title">Sign In</h1>
              <form action="" name="" method="" class="login-form mt-4">
                <div class="form-group">
                  <input type="text" class="form-control login-input" name="username" id="username" placeholder="Username">
                </div>
                  <div class="form-group">
                    <div class="input-group">
                      <input type="password" class="form-control login-input" name="password" id="password" placeholder="Password">
                        <div class="input-group-append">
                          <span class="input-group-text bg-transparent">
                            <span class="zmdi zmdi-eye toggle-password"></span>
                          </span>
                        </div>
                    </div>
                  </div>
                  <div class="form-group">
                    <button type="submit" class="btn btn-login mt-4">Sign in</button>
                  </div>
                  Dont have any account ?
                  <a href="/register" class="register-link mt-4" style="text-decoration: none; color: #1E90FF;"> Register </a>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.login {
    padding-top: 150px;
    padding-bottom: 100px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #ececec;
}
.login-card {
    margin: auto;
    padding: 40px;
}
.login-title {
    font-size: 50px;
    color: #080808;
    text-align: center;
}
.login-input {
    border-radius: 0px;
    padding: 25px;
    font-size: 20px;
}
.btn-login {
    background-color:dodgerblue;
    color: #ececec;
    padding: 15px 50px;
    border-radius: 50px;
    transition: 0.3s ease;
}
.btn-login:hover {
    background-color: transparent;
    color: #080808;
    border: 1px solid #080808;
}
</style>

