# Class Photos by Graduation year

Select Graduation Year: 
<select id="grad_year" onchange="load_photos()">
	<option value="2018">2018</option>
	<option value="2017">2017</option>
	<option value="2016">2016</option>
	<option value="2015">2015</option>
</select>
*Note: Put in the year you would have graduated, without skipping any grades. *
*For example, if you were in 5th grade in 2009-2010, select 2017 even if you graduated in 2016*

<div id="5th_pics">
</div>


<script>
	img_folder = "/pegs-history/media/images/";
	function load_photos() {
		sel = document.getElementById("grad_year");
		var sel_grad_yr = sel.value;
		var 5th_year = sel_grad_yr - 7;
		// Load the appropriate year's pictures
		alert("Selected: "+sel_grad_yr);
		
		img_src = img_folder+(5th_year-1)+"_"+5th_year+"_g5_trim.jpg";
		alt_text = "5th grade "+(5th_year-1)+"-"+5th_year;
		
		document.getElementById("5th_pics").innerHTML = "<img src="+img_src+" alt="+alt_text" />";
		
	}
	/*
	sel = document.getElementById("grad_year");
	sel.addEventListener("change", function(e){
		// Load the appropriate year's pictures
		alert("Selected":);
	});*/
</script>
<!--
[2016](./2016.html)
[2015](./2015.html)
-->
