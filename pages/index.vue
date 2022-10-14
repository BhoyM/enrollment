<template>
        <div class="row">
          <div class="col-lg-5 m-auto">
            <div class="card mt-5 bg-dark">
              <img class="rounded-sm w-55 h-55 border rounded-circle mx-auto d-block" src="avatar.png">
              <div class="card-body">
                <form>
                  <div class="input-group mb-3">
                    <div class="input-group-prepend">
                      <span class="input-group-text">
                        <i class="fa fa-user fa-2x"></i>
                      </span>
                    </div>
                    <input type="text" class="form-control py-4" placeholder="User Name">
                  </div>
                  <div class="input-group mb-3">
                    <div class="input-group-prepend">
                      <span class="input-group-text">
                        <i class="fa fa-lock fa-2x"></i>
                      </span>
                    </div>
                    <input type="text" class="form-control py-4" placeholder="User Password">
                  </div>
                  <button class="btn btn-success">Login Now</button>
                  <p class="float-right text-white mt-2"><input type="checkbox">Remember Me</p>
                </form>
              </div>
            </div>
          </div>
        </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>


