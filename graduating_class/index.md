# Class Photos by Graduation year

Select the year you were in *first grade*: 
<select id="1st_year" onchange="load_photos()">
	<option value="2006">2018</option>
	<option value="2005">2017</option>
	<option value="2004">2016</option>
	<option value="2003">2015</option>
</select>

*Note: We would have said put in your graduating class, 
*but with all the grade skipping, that doesn't make much sense.

<!--*Note: Put in the year you would have graduated, without skipping any grades. 
*For example, if you were in 5th grade in 2009-2010, select 2017 even if you graduated in 2016-->

We haven't uploaded most of the class pictures yet, so if they're here, then congratulations. 
If not, look in the shared [PEGS History google photos album](https://photos.google.com/share/AF1QipP3AVw6w-Ee8S4nkstATMq4AlQ6uB5JAQFLAI-ufwojwftqZPv52eHemkumOgt2sw?key=YUhFSHRIcVRSMDhHckZTajFXbThOTDdjR0NMMkNR)

<div id="5th_pics">
</div>

<script>
	alert("Test1");
	img_folder = "/pegs-history/media/images/";
	function load_photos() {
		alert("Test2")
		sel = document.getElementById("1st_year");
		var sel_1st_yr = sel.value;
		var 5th_year = sel_1st_yr + 4;
		// var 5th_year = sel_grad_yr - 7;
		// Load the appropriate year's pictures
		alert("Selected: "+sel_1st_yr);
		
		img_src = img_folder+(5th_year-1)+"_"+5th_year+"_g5_trim.jpg";
		alt_text = "5th grade "+(5th_year-1)+"-"+5th_year;
		
		document.getElementById("5th_pics").innerHTML = "<img src="+img_src+" alt="+alt_text" />";
	}
	/* Alternative method
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
