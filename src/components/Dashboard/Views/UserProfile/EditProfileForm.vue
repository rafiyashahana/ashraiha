<template>
  <div class="card">
    <div class="header">
      <h4 class="title">Company Details</h4>
    </div>
    <div class="content">
      <form>
        

        <div class="row">
          <div class="col-md-6">
            <fg-input type="text"
                      label="Company Name"
                      placeholder="Company Name"
                      v-model="user.cname">
            </fg-input>
          </div>
          <div class="col-md-6">
            <fg-input type="text"
                      label="TIN No."
                      placeholder="TIN No."
                      v-model="user.tin">
            </fg-input>
          </div>
        </div>

        <div class="row">
          <div class="col-md-12">
            <fg-input type="text"
                      label="Address"
                      placeholder="Address"
                      v-model="user.address">
            </fg-input>
          </div>
        </div>

        <div class="row">
          <div class="col-md-4">
            <fg-input type="text"
                      label="City"
                      placeholder="City"
                      v-model="user.city">
            </fg-input>
          </div>
          <div class="col-md-4">
            <fg-input type="text"
                      label="State"
                      placeholder="State"
                      v-model="user.state">
            </fg-input>
          </div>
          <div class="col-md-4">
            <fg-input type="number"
                      label="Postal Code"
                      placeholder="ZIP Code"
                      v-model="user.postalCode">
            </fg-input>
          </div>
        </div>

        <div class="row">
          <div class="col-md-7">
            <fg-input type="text"
                      label="Email"
                      placeholder="Email"
                      v-model="user.email">
            </fg-input>
          </div>

          <div class="col-md-5">
            <fg-input type="text"
                      label="Phone"
                      placeholder="Phone"
                      v-model="user.phone">
            </fg-input>
          </div>
        </div>

        <div class="row">
          <div class="col-md-12">
            <div class="form-group">
              <label>Additional Details</label>
              <textarea rows="5" class="form-control border-input"
                        placeholder="(Optional)"
                        v-model="user.aboutMe">

              </textarea>
            </div>
          </div>
        </div>
        <div class="text-center">
          <button type="submit" class="btn btn-info btn-fill btn-wd" @click.prevent="updateProfile">
            Create Profile
          </button>
        </div>
        <div class="clearfix"></div>
      </form>
    </div>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        user: {
          cname: '',
          tin: '',
          address: '',
          city: '',
          state: 'Karnataka',
          postalCode: 'melbourne',
          email: '',
          phone: '',
          aboutMe: ``
        }
      }
    },
    methods: {
      updateProfile () {
        alert('Your data: ' + JSON.stringify(this.user))
      }
    }
  }

</script>
<style>

</style>
