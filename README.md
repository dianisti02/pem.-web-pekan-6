# pem.-web-pekan-6
image picker,
login authentication,
form validation.

<!DOCTYPE html>
<html>
    <head>
        <title>IMAGE PICKER</title>
    </head>
    <body style="margin: 200px"> 	
    <center>		
    <select onchange="gantigambar();" id="listgambar">			
    <option value="https://upload.wikimedia.org/wikipedia/commons/d/dd/Genshin_Impact_logo.png">PILIH KARAKTER</option>			
    <option value="https://uploadstatic-sea.mihoyo.com/contentweb/20200616/2020061611214389168.png">JEAN</option>			
    <option value="https://uploadstatic-sea.mihoyo.com/contentweb/20191009/2019100914372396510.png">AMBER</option>			
    <option value="https://uploadstatic-sea.mihoyo.com/contentweb/20191009/2019100915122465321.png">LISA</option>			
    <option value="https://uploadstatic-sea.mihoyo.com/contentweb/20191009/2019100910335338023.png">KAEYA</option>			
    <option value="https://uploadstatic-sea.mihoyo.com/contentweb/20200609/2020060915105884221.png">DILUC</option>			
    <option value="https://uploadstatic-sea.mihoyo.com/contentweb/20200103/2020010310582722822.png">KLEE</option>		
    </select>	
    
    
    </center>		
    
    <br/>	
    
    <img src="https://upload.wikimedia.org/wikipedia/commons/d/dd/Genshin_Impact_logo.png" style="width: 700%" id="gambar"> 
    </body>
        
    <script type="text/javascript">	
    function gantigambar() {		
    let gambar =
document.getElementById("listgambar").value;
document.getElementById("gambar").src = gambar;		alert("Ini Gambar " + gambar);}

</script>
    
</html>




<!DOCTYPE html>
<html>
    <head>
        <title>LOGIN</title>
    </head>
    <body style="margin: 200px">
        
    <center>
         <form method="REQUEST">Username:
         <br/>
			
<input type="text" placeholder="username" id="username" name="username"><br/>Password<br/>
			
<input type="password"  placeholder="password" id="password" name="password"><br/>
    
    
    <button type="submit" onclick="return login()">SUBMIT</button>
        
        
        
    </form>
	</center>

</body>

<script type="text/javascript">
	function login() {
		username = document.getElementById("username").value;
		password = document.getElementById("password").value;

		if (username == "" || password == "") {
			alert("Username / Password Tidak Boleh Kosong");
			return false;
		}
		else if (password.length < 6) {
			alert("Password Kurang dari 6");
			return false;
		}
		else if (username == "Dian" && password == "123456789") {
			window.location = "chat.html";
			return false;
		}else{
			alert("Username / Password anda salah");
		}
	}
</script>
</html>
