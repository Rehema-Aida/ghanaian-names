# ghanaian-names
Here I learn how to attach names to date of birth using JS,HTML and CSS
Akan names are Ghanaian names given to children based on the day of the week they are born.
My project is licensed by MIT License, Copytright Rehema Aida 2019.
Illustration of my JS code.

<script LANGUAGE="JavaScript">
</script>

var date;
var month;
var year;
var century;
var gender;
var dayOfWeek;
var maleNames = ['Kwasi','Kwadwo','Kwabena','Kwaku','Yaw','Kofi','Kwame'];
var femaleNames = ['Akosua','Adwoa','Abenaa','Akua','Yaa','Afua','Ama'];

var gender = ['m','f'];

var result = function(){
   dayOfWeek = calculate();
}

var day = function(){
dd = parseInt(document.getElementById("dd").value);
mm = parseInt(document.getElementById("mm").value);
yy = parseInt(document.getElementById("yy").value);
cc = parseInt(document.getElementById("cc").value);
}

let dd = parseInt(form.dd.value)
if ((dd<0)||(dd>31)){
   alert ('Wrong date');
}

let mm = parseInt(form.mm.value)
if ((mm<0)||(mm>12)){
   alert('Wrong Month');
}

function calculate(){
   day()
   dayofWeek  = ( ( (cc/4) -2*cc-1) + ((5*yy/4) ) + ((26*(mm+1)/10)) + dd ) % 7;
   return(Math.floor(dayofWeek));
   console.log(dayofWeek);
}

switch(gender){
   case 'm':
            if(dayOfWeek == 0){
               document.getElementById("result").innerHTML = "Sunday" + MaleNames['Kwasi'];
            }else if (day == 1){
               document.getElementById("result").innerHTML = "Monday" + maleNames['Kwadwo'];
            }else if (day == 2){ 
               document.getElementById("result").innerHTML = "Tuesday" + maleNames['Kwabena'];
            }else if (day == 3){ 
               document.getElementById("result").innerHTML = "Wednesday" + maleNames['Kwaku'];
            }else if (day == 4){ 
               document.getElementById("result").innerHTML = "Thursday" + maleNames['Yaw'];
            }else if (day == 5){ 
               document.getElementById("result").innerHTML = "Friday" + maleNames['Kofi'];
            }else { 
               document.getElementById("result").innerHTML = "Saturday" + maleNames['Kwame'];
   }
break;
   case "f":
            if(dayofWeek == 0){
                document.getElementById("result").innerHTML = "Sunday" + femaleNames['Akosua'];
            }else if (day == 1){
                document.getElementById("result").innerHTML = "Monday" + femaleNames['Adwoa'];
            }else if (day == 2){ 
                document.getElementById("result").innerHTML = "Tuesday" + femaleNames['Abenaa'];
            }else if (day == 3){ 
                document.getElementById("result").innerHTML = "Wednesday" + femaleNames['Akua'];
            }else if (day == 4){ 
                document.getElementById("result").innerHTML = "Thursday" + femaleNames['Yaa'];
            }else if (day == 5){ 
                document.getElementById("result").innerHTML = "Friday" + femaleNames['Afua'];
            }else{ 
                document.getElementById("result").innerHTML = "Saturday" + femaleNames['Ama'];
            }
break;
         }
