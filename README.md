# RK_3

<html>
<head/>
<body> 
	<canvas id='RK3' width='700' height='300'>
           <script>
		function degToRad (deg) { return deg / 180 * Math.PI; }
		document.write("Pi is approximately equal to " + Math.PI);
                var canvas = document.getElementById('RK3');
                var ctx = canvas.getContext('2d');
		var x=50,y=70;
		var x1,y1, x2, x3,y3;		
		ctx.fillRect(x,y,5,5);
		ctx.fillStyle='#0000FF';
		x1=x*Math.cos(degToRad(30))-y*Math.sin(degToRad(30));
		y1=x*Math.sin(degToRad(30))+y*Math.cos(degToRad(30));
		ctx.fillRect(x1,y1,5,5);
		ctx.fillStyle='#FF0000';
		x2=x+50;
		ctx.fillRect(x2,y1,5,5);
		ctx.fillStyle='#00FF00';
		x3=x*Math.cos(degToRad(-30))-y*Math.sin(degToRad(-30));
		y3=x*Math.sin(degToRad(-30))+y*Math.cos(degToRad(-30));
		ctx.fillRect(x3,y3,5,5);
		alert("Начальные координаты точки: ("+x+" , "+y+")");
		alert("Координаты точки после поворота на 30 гр(синий): ("+x1+" , "+y1+")");
		alert("Координаты точки после сдвига (красный): ("+x2+" , "+y1+")");
		alert("Координаты точки после поворота на -30гр (зеленый): ("+x3+" , "+y3+")");
       </script>     
</canvas>
</body>
</html>
