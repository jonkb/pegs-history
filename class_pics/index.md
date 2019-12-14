# Class Photos by Graduation year

Select the year you were in *first grade*: 
<select id="first_year"> <!-- onchange="load_photos();">-->
	<option value="2006">2006</option>
	<option value="2005">2005</option>
	<option value="2004">2004</option>
	<option value="2003">2003</option>
</select>

*Note: We would have said put in your graduating class, 
*but with all the grade skipping, that doesn't make much sense.

<!--*Note: Put in the year you would have graduated, without skipping any grades. 
*For example, if you were in 5th grade in 2009-2010, select 2017 even if you graduated in 2016-->

We haven't uploaded most of the class pictures yet, so if they're here, then you're in luck. 
If not, look in the shared [PEGS History google photos album](https://photos.google.com/share/AF1QipP3AVw6w-Ee8S4nkstATMq4AlQ6uB5JAQFLAI-ufwojwftqZPv52eHemkumOgt2sw?key=YUhFSHRIcVRSMDhHckZTajFXbThOTDdjR0NMMkNR)

<div id="fifth_pics">
</div>

<script>
	alert("Test1");
	img_folder = "/pegs-history/media/images/";
	function load_photos(e) {
		alert("Test2")
		sel = document.getElementById("first_year");
		var first_yr = sel.value;
		alert("Selected: "+first_yr);
		var fifth_year = first_yr + 4;
		// var fifth_year = sel_grad_yr - 7;
		
		img_src = img_folder+(fifth_year-1)+"_"+fifth_year+"_g5_trim.jpg";
		alt_text = "5th grade "+(fifth_year-1)+"-"+fifth_year;
		
		document.getElementById("fifth_pics").innerHTML = "<img src="+img_src+" alt="+alt_text" />";
	}
	
	sel = document.getElementById("first_year");
	sel.onchange = load_photos;
	//sel.addEventListener("change", load_photos);
</script>
<!--
[2016](./2016.html)
[2015](./2015.html)
-->
