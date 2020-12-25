<!-- Generated Card UI added here -->
<template>
  <div class="section-container section-right col-6">
    <div class="id-card-container" id="collegeCard">
      <div class="text-center subtitle-card">Generated ID Card</div>
      <div class="card-container">
        <div class="card-wrapper">
          <div class="user-card">
            <span class="user-photo">
              <i class="fa fa-user"></i>
            </span>
          </div>
          <div class="general-information text-left">
            <div class="card-element card-name">
              <span class="card-title">Name: </span>
              <span class="card-input" id="cardName">{{formData.fullName}}</span>
            </div>
            <div class="card-element college-name">
              <span class="card-title">College Name: </span>
              <span class="card-input" id="cardCollegeName">{{formData.collegeName}}</span>
            </div>
            <div class="card-element college-name">
              <span class="card-title">Location: </span>
              <span class="card-input" id="cardLocation">{{formData.locationName}}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GeneratedCard',
  props: {
      formData: Object
  }
}
</script>