<template>
  <div class="panel">
    <div class="panel-element">
      <div class="element-actions">
        <button class="btn btn-action btn-hide"><i class="fa fa-ban"></i></button>
        <button class="btn btn-action btn-heart"><i class="fa fa-heart-o"></i></button>
      </div>
      <div class="element-content">
        <button class="btn btn-more">
          <i class="fa fa-ellipsis-h icon-closed"></i>
          <i class="fa fa-times icon-open"></i>
          <i class="fa fa-heart-o icon-hearted"></i>
        </button>
        <div class="content-post">
          <div class="post-avatar"></div>
          <div class="post-content">
            <span class="post-title">Lorem Ipsum Dolor Sit</span>
            <p class="post-body">Amet consectetur adipiscing elit vestibulum lacinia nibh id sem.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  // @ is an alias to /src

  export default {
    name: 'About'
  }
</script>

<style>
  /* Reset */
@import url(//codepen.io/chrisdothtml/pen/ojLzJK.css);
/* Extenders */
.clearfix:after, .panel .panel-element .element-content .content-post:after, .panel .panel-element .element-actions:after {
  content: '';
  display: table;
  clear: both;
}
.animate, .panel .panel-element .element-content, .panel .panel-element .element-content .btn-more, .panel .panel-element .element-actions .btn-action, .panel .panel-element .element-actions .btn-action > i {
  transition: all 0.2s;
}
/* General */
button {
  display: block;
  background: transparent;
  border: 0;
  cursor: pointer;
}
h1 {
  display: block;
  background-color: #fff;
  width: 100%;
  line-height: 1;
  margin-bottom: 20px;
  padding: 65px 50px;
  font-weight: 700;
  font-size: 32px;
  color: #6F6F6F;
}
.panel {
  max-width: 450px;
  margin: 0 auto;
  padding: 30px 20px;
}
.panel .panel-element {
  position: relative;
}
.panel .panel-element .element-content {
  background-color: #fff;
  padding: 15px;
  border-bottom: 1px solid #d6d6d6;
  position: relative;
  right: 0;
  z-index: 2;
}
.panel .panel-element .element-content .btn-more {
  width: 30px;
  height: 30px;
  line-height: 30px;
  opacity: 0;
  position: absolute;
  top: 0;
  right: 0;
}
.panel .panel-element .element-content .btn-more > i {
  font-size: 16px;
  color: #929292;
  vertical-align: middle;
}
.panel .panel-element .element-content .btn-more .icon-open, .panel .panel-element .element-content .btn-more .icon-hearted {
  display: none;
}
.panel .panel-element .element-content .btn-more:hover {
  background-color: #F9F9F9;
}
.panel .panel-element .element-content .content-post .post-avatar {
  background-color: #ededed;
  width: 60px;
  height: 60px;
  float: left;
  border-radius: 50%;
}
.panel .panel-element .element-content .content-post .post-content {
  margin-left: 75px;
  padding-top: 9px;
}
.panel .panel-element .element-content .content-post .post-content .post-title, .panel .panel-element .element-content .content-post .post-content .post-body {
  display: block;
}
.panel .panel-element .element-content .content-post .post-content .post-title {
  font-size: 14px;
  color: #AFADAD;
}
.panel .panel-element .element-content .content-post .post-content .post-body {
  margin-top: 5px;
  font-size: 12px;
  color: #CCCBCB;
}
.panel .panel-element .element-content:hover .btn-more {
  opacity: 1;
}
.panel .panel-element .element-actions {
  width: 100px;
  height: 45px;
  font-size: 0;
  position: absolute;
  top: 50%;
  right: 20px;
  z-index: 1;
  transform: translateY(-50%);
}
.panel .panel-element .element-actions .btn-action {
  display: inline-block;
  width: 45px;
  height: 45px;
  border-width: 2px;
  border-style: solid;
  border-radius: 50%;
}
.panel .panel-element .element-actions .btn-action > i {
  font-size: 20px;
}
.panel .panel-element .element-actions .btn-action.btn-hide {
  border-color: #34495e;
}
.panel .panel-element .element-actions .btn-action.btn-hide > i {
  color: #34495e;
}
.panel .panel-element .element-actions .btn-action.btn-hide:hover {
  background-color: #34495e;
}
.panel .panel-element .element-actions .btn-action.btn-heart {
  border-color: #e74c3c;
}
.panel .panel-element .element-actions .btn-action.btn-heart > i {
  color: #e74c3c;
}
.panel .panel-element .element-actions .btn-action.btn-heart:hover {
  background-color: #e74c3c;
}
.panel .panel-element .element-actions .btn-action:not(:last-child) {
  margin-right: 10px;
}
.panel .panel-element .element-actions .btn-action:hover > i {
  color: #fff;
}
.panel .panel-element:not(:first-child) {
  margin-top: 15px;
}
.panel .panel-element.panel-element-open .element-content {
  right: 140px;
}
.panel .panel-element.panel-element-open .element-content .btn-more {
  opacity: 1;
}
.panel .panel-element.panel-element-open .element-content .btn-more .icon-closed {
  display: none;
}
.panel .panel-element.panel-element-open .element-content .btn-more .icon-open {
  display: inline-block;
}
.panel .panel-element.panel-element-hearted .element-actions .btn-action.btn-heart {
  background-color: #e74c3c;
}
.panel .panel-element.panel-element-hearted .element-actions .btn-action.btn-heart > i {
  color: #fff;
}
.panel .panel-element.panel-element-hearted .element-content .btn-more {
  opacity: 1;
}
.panel .panel-element.panel-element-hearted .element-content .btn-more > i {
  color: #e74c3c;
}
.panel .panel-element.panel-element-hearted .element-content .btn-more .icon-open, .panel .panel-element.panel-element-hearted .element-content .btn-more .icon-closed {
  display: none;
}
.panel .panel-element.panel-element-hearted .element-content .btn-more .icon-hearted {
  display: inline-block;
}
@media screen and (max-width: 500px) {
  h1 {
    margin-bottom: 0;
    padding: 40px;
    font-size: 25px;
  }
  .panel .panel-element .element-content .btn-more {
    opacity: 1;
  }
  .panel .panel-element .element-content .btn-more:hover {
    background-color: transparent;
  }
}

</style>
