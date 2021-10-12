<template>
<div>
  <div id="wrapper">
    
    <NavHorizontal />
    <NavVertical/>
    
  </div>
<div class="container">



      <div class="d-sm-flex align-items-center justify-content-between mb-4">
        <h1 class="h3 mb-0 text-gray-800">Empresas</h1>
      </div>

      <div class="row">


        <div class="col-xl-3 col-md-6 mb-4">
          <div class="card border-left-primary shadow h-100 py-2">
            <div class="card-body">
              <div class="row no-gutters align-items-center">
                <div class="col mr-2">
                  <div
                    class="
                      text-xs
                      font-weight-bold
                      text-primary text-uppercase
                      mb-1
                    "
                  >
                    Earnings (Monthly)
                  </div>
                  <div class="h5 mb-0 font-weight-bold text-gray-800">
                    $40,000
                  </div>
                </div>
                <div class="col-auto">
                  <i class="fas fa-calendar fa-2x text-gray-300"></i>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Earnings (Annual) Card Example -->
        <div class="col-xl-3 col-md-6 mb-4">
          <div class="card border-left-success shadow h-100 py-2">
            <div class="card-body">
              <div class="row no-gutters align-items-center">
                <div class="col mr-2">
                  <div
                    class="
                      text-xs
                      font-weight-bold
                      text-success text-uppercase
                      mb-1
                    "
                  >
                    Earnings (Annual)
                  </div>
                  <div class="h5 mb-0 font-weight-bold text-gray-800">
                    $215,000
                  </div>
                </div>
                <div class="col-auto">
                  <i class="fas fa-dollar-sign fa-2x text-gray-300"></i>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

</div>
</template>

<script>
import NavVertical from "@/components/NavVertical";
import NavHorizontal from "@/components/NavHorizontal";


export default {
  name: "About",

  data() {},

  components: {
    NavHorizontal,
    NavVertical
  
  },
};
</script>



<style scoped src="@/css/estylo.css">



</style>