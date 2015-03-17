# Js
Window scroll
<script>
$(document).ready(function(){
	// hide #backToTop first
	$("#backToTop").hide();
	
	// fade in #backToTop
	$(function () {
		$(window).scroll(function () {
			if ($(this).scrollTop() > 100) {
				$('#backToTop').fadeIn();
			} else {
				$('#backToTop').fadeOut();
			}
		});
		// scroll body to 0px on click
		$('#backToTop a').click(function () {
			$('body,html').animate({
				scrollTop: 0
			}, 800);
			return false;
		});
	});
});
</script>
