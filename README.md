# jQuery-Accordion
jQuery Accordion + -

https://codepen.io/vikasverma93/pen/raxGaM
...........................html...................................


<div class="accordion-container">
  <h2>jQuery Accordion</h2>
  <div class="set">
    <a href="#">
      Vestibulum 
      <i class="fa fa-plus"></i>
    </a>
    <div class="content">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.</p>
    </div>
  </div>
  <div class="set">
    <a href="#">
      Phasellus 
      <i class="fa fa-plus"></i>
    </a>
    <div class="content">
      <p> Aliquam cursus vitae nulla non rhoncus. Nunc condimentum erat nec dictum tempus. Suspendisse aliquam erat hendrerit vehicula vestibulum.</p>
    </div>
  </div>
  <div class="set">
    <a href="#">
      Praesent 
      <i class="fa fa-plus"></i>
    </a>
    <div class="content">
      <p>Pellentesque aliquam ligula libero, vitae imperdiet diam porta vitae. sed do eiusmod tempor incididunt ut labore et dolore magna.</p>
    </div>
  </div>
  <div class="set">
    <a href="#">
      Curabitur 
      <i class="fa fa-plus"></i> 
    </a>
    <div class="content">
      <p> Donec tincidunt consectetur orci at dignissim. Proin auctor aliquam justo, vitae luctus odio pretium scelerisque. </p>
    </div>
  </div>
</div>
....................html.......................

..................js.........................

$(document).ready(function() {
  $(".set > a").on("click", function() {
    if ($(this).hasClass("active")) {
      $(this).removeClass("active");
      $(this)
        .siblings(".content")
        .slideUp(200);
      $(".set > a i")
        .removeClass("fa-minus")
        .addClass("fa-plus");
    } else {
      $(".set > a i")
        .removeClass("fa-minus")
        .addClass("fa-plus");
      $(this)
        .find("i")
        .removeClass("fa-plus")
        .addClass("fa-minus");
      $(".set > a").removeClass("active");
      $(this).addClass("active");
      $(".content").slideUp(200);
      $(this)
        .siblings(".content")
        .slideDown(200);
    }
  });
});

.......................js...............................

....................css.......................
body{
  background-color: #567;
  padding: 0 10px;
  font-family: 'Open Sans', sans-serif;
}
.accordion-container{
  position: relative;
  max-width: 500px;
  height: auto;
  margin: 10px auto;
}
.accordion-container > h2{
  text-align: center;
  color: #fff;
  padding-bottom: 5px;
  margin-bottom: 20px;
  padding-bottom: 15px;
  border-bottom: 1px solid #ddd;
}
.set{
  position: relative;
  width: 100%;
  height: auto;
  background-color: #f5f5f5;
}
.set > a{
  display: block;
  padding: 10px 15px;
  text-decoration: none;
  color: #555;
  font-weight: 600;
  border-bottom: 1px solid #ddd;
  -webkit-transition:all 0.2s linear;
  -moz-transition:all 0.2s linear;
  transition:all 0.2s linear;
}
.set > a i{
  float: right;
  margin-top: 2px;
}
.set > a.active{
  background-color:#3399cc;
  color: #fff;
}
.content{
  background-color: #fff;
  border-bottom: 1px solid #ddd;
  display:none;
}
.content p{
  padding: 10px 15px;
  margin: 0;
  color: #333;
}
......................css...................
