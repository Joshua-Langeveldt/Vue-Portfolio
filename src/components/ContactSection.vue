<template>
      <div class="containing">
        <div class="row mb-5">
          <div class="col-12 text-center">
          </div>
        </div>
        <div class="row">
          <div class="col-md-12 mb-5">



            <form action="https://formspree.io/f/xwkgzvvb" method="POST" class="p-5">


              <div class="row form-group">
                <div class="col-md-6 mb-3 mb-md-0">
                  <label class="text-cust" for="fname">First Name</label>
                  <input type="text" id="fname" class="form-control">
                </div>
                <div class="col-md-6">
                  <label class="text-cust" for="lname">Last Name</label>
                  <input type="text" id="lname" class="form-control">
                </div>
              </div>

              <div class="row form-group">

                <div class="col-md-12">
                  <label class="text-cust" for="email">Email</label>
                  <input type="email" id="email" class="form-control">
                </div>
              </div>

              <div class="row form-group">

                <div class="col-md-12">
                  <label class="text-cust" for="subject">Subject</label>
                  <input type="subject" id="subject" class="form-control">
                </div>
              </div>

              <div class="row form-group">
                <div class="col-md-12">
                  <label class="text-cust" for="message">Message</label>
                  <textarea name="message" id="message" cols="30" rows="7" class="form-control" placeholder="Write your notes or questions here..."></textarea>
                </div>
              </div>

              <div class="row form-group">
                <div class="col-md-12">
                  <input type="submit" value="Send Message" class="btn btn-dark btn-md text-white">
                </div>
              </div>


            </form>
          </div>

        </div>
      </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.contactContainer {
    padding: 60px 0;
    background: linear-gradient(to bottom,#7B3F00,  #d1691d, #ff5349);
}



.containing {
    max-width: 960px;
    margin: 0 auto;
    padding: 15px;
}

.text-center {
    text-align: center;
}

/* Form Styles */

form {
    padding: 30px;
    border-radius: 4px;
}

.form-control {
    width: 100%;
    padding: 10px;
    border: 2px solid black;
    border-radius: 4px;
    margin-bottom: 10px;
}

.btn-primary {
    background: #007bff;
    border: none;
    color: #fff;
    padding: 10px 20px;
    border-radius: 4px;
    cursor: pointer;
}

.p-5{

    background: linear-gradient(to bottom,#7B3F00,  #d1691d, #ff5349);
    padding: 2rem;
}

.text-cust{
    color: white;
    margin: 10px;
    font-family: "Italiana", sans-serif;
  font-weight: 400;
  font-style: normal;
      font-size: 1rem;

}


</style>