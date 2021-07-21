<template>
  <div class="card">
    <div class="card-body">
        <div class="row" style="height:20vh">
            <div class="col-md-3 ">
                <slot name="left"/>
            </div>
            <div class="col-md-4">
                <slot name="middle"/>
            </div>
            <div class="col-md-3">
                <slot name="right"/>
            </div>
        </div>
    </div>
  </div>
</template>