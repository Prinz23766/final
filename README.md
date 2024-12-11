<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            background-color: #2b2b2b;
  margin: 0;
}

    
.header {
    background: linear-gradient(120deg, #1a1d23, #3a3f4b);
    padding: 20px 50px;
    text-align: center;
    color: aliceblue;
    display: flex;
    justify-content: center; /* Centers horizontally */
    align-items: center; /* Centers vertically */
    width: 100%;
    box-sizing: border-box;
}

.logo-container {
    display: flex;
    align-items: center;
    gap: 10px; /* Space between the logo and text */
}

        .header img {
          display: flex;
align-items: center;
          text-align: center;
            height: 80px;
            width: 80px;
            border-radius: 50%;
            margin-right: 20px;
        }

        .header h1 {
            font-family: 'Times New Roman', Times, serif;
            font-size: 32px;
            color: white;
            display: inline;
        }

        .topnav{
            border: #555555;
            overflow:hidden;
            background-color:#333333;
            color: aliceblue;
            font-family: Georgia, 'Times New Roman', Times, serif;

        }
        .topnav a{
            float: left;
            display: block;
            color: antiquewhite;
            text-align: center;
            padding: 15px 20px;
            text-decoration: double;
            font-family: Georgia, 'Times New Roman', Times, serif;
        }
        .topnav :hover{
            
            color: #555555;
        }
        .body{
            flex-grow:1;
            padding:10px;
            background-color:#2b2b2b;
            overflow: hidden;
            
        }
        #outerbox{
            width:250px;
            overflow: hidden;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            border-radius: 10px;
            background-position:center;width: 450;
            margin:10px auto;
            box-shadow:10px 15px 20px;
            
           
           
        
        }
        #slidebox{
            
            position: relative;
            display: flex;
            width:1000px;
            height: 4500;
            animation:slider 30s infinite;
            

           
            
        }
        

        @keyframes slider {

            0% {
                left: 0px;
            }

            11% {
                left: -250px;
            }

            22% {
                left: -500px;
            }

            33% {
                left: -750px;
            }

            44% {
                left: -1000px;
            }

            55% {
                left: -1250px;
            }

            66% {
                left: -1500px;
            }

            77% {
                left: -1750px;
            }

            88% {
                left: -2000px;
            }

            100% {
                left: -2250px;
            }
        }

        #slidebox img {
            width: 1000px;
            height: 250px;
            align-items: center;
            justify-content: center;
            
        }
    .open-modal
    {
    padding: 10px 15px;
    background-color:none;
    color: white;
    text-align: center;
    border: none;
    cursor: pointer;
    border-radius: 5px;
    float: right;
    text-decoration: none;
}
.open-modal:hover{
    background-color: none;
}


.modal{
    display: none;
    position: fixed;
    z-index: 1;
    left: 0%;
    top: 0%;
    width: 100%;
    height:100vh;
    overflow: none;
    backdrop-filter: blur(5px);
    background-color: transparent;
}
.modal-toggle{
    display: none;
}
.modal-toggle:checked + .modal{
    display: block;
}
.modal-content{
    background-color: rgb(218, 208, 253);
    margin-top: 15%;
    margin: 10% auto;
    padding: 15px;
    border: 1px solid #888;
    width:300px;
    border-radius: 5px;
    position: relative;
    height: 350px;
}
.close{
color: #aaa;
float: right;
font-size: 28px;
font-weight: bold;
color: pointer;
}
.close:hover{
    color:black;
}
.form{
    display: flex;
    flex-direction: column;
}
.form:hover{
    background-color: transparent;
}
.label{
    margin: 10px 0 5px;
}
input[type="text"],
input[type="password"]{
padding: 10px;
margin-bottom: 15px;
border: 1px solid #ccc;
border-radius: 4px;
}
button[type="log-in"]{
    background-color: lawngreen;
    border: none;
    padding: 10px;
    color: white;
    border-radius: 5px;
    cursor: pointer;
}
button[type="Register"]{
    background-color: lawngreen;
    border: none;
    padding: 10px;
    color: white;
    border-radius: 5px;
    cursor: pointer;
}
button[type="submit"]:hover{
background-color: #888;
}
.bottom{
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: #232526;
    padding-top: 5px;
    padding-bottom: 5px;
    color: white;
}

        .gallery {
  display: flex;
  justify-content: center;
  align-items: center;
  perspective: 1200px;
  width: 100vw;
  height: 40vh; /* Ensure the gallery takes full viewport height */
}

.gallery-container {
    width: 200px;  /* Make the container relative to the viewport */
    height: 200px; /* Make the container relative to the viewport */
  position: relative;
  transform-style: preserve-3d;
  animation: rotate 15s infinite linear;
  transform-origin: center center; /* Ensures rotation is centered */
}

.gallery-image {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  border-radius: 10px; /* Rounded corners for images */
}

.gallery-image img {
  width: 100%;
  height: 100%;
  object-fit: contain; /* Ensures images fit within the container */
  border-radius: 10px;
}

.gallery-image:nth-child(1) { transform: rotateY(0deg); }
.gallery-image:nth-child(2) { transform: rotateY(90deg); }
.gallery-image:nth-child(3) { transform: rotateY(180deg); }
.gallery-image:nth-child(4) { transform: rotateY(-90deg); }

@keyframes rotate {
  0% { transform: rotateY(0deg); }
  100% { transform: rotateY(360deg); }
}

/* Thumbnail Gallery */
.thumbnail-gallery {

  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  justify-content: center;
  margin-top: 20px;
}

/* Responsive Styles */
@media (max-width: 768px) {
  .gallery-container {
    width: 70vw;
    height: 70vh;
  }
}
.thumbnail {
      position: relative;
      overflow: hidden;
      width: 100px;
      height: 100px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
    }

    .thumbnail img {
      width: 100%;
      height: 100;
      display: block;
    }

    .thumbnail:hover {
      transform: scale(1.1);
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
    }
    .description {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      background: rgba(0, 0, 0, 0.6);
      color: white;
      text-align: center;
      font-style: initial;
      font-size: 15px;
      padding: 5px;
      opacity: 0;
      transition: opacity 0.3s ease;
    }

    .thumbnail:hover .description {
      opacity: 1;
    }
     .thumbnail {
        width: 150px;
        height: 100%;
      }

    .description {
        font-size: 9px;
}
footer {
            background: black;
            color: white;
            text-align: center;
            padding: 5px;
            position: relative;
            bottom: 0;
            width: 100%;
        }
        body::-webkit-scrollbar{
  display: none;
}


.logo-image {
    width: 50px; /* Adjust size as needed */
    height: auto;
}
.background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            backdrop-filter: blur(0px);
            transition: backdrop-filter 0.5s ease;
            z-index: 1;
        }

        /* Navigation with Login Button (aligned to right) */
        .open-login {
            position: absolute;
            top: 127px;
            right: 20px; /* Align to the right */
            z-index: 2;
        }

        .open-login button {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .open-login button:hover {
            background-color: #0056b3;
        }

        /* Form Container Styling */
        .form-container {
    background: white;
    padding: 20px;
    width: 100%;
    max-width: 400px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    border-radius: 8px;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%); /* Centers the form in both directions */
    z-index: 3;
    display: none;
}

        

        .form-container.active {
            display: block;
        }

        h2 {
            margin-bottom: 15px;
            text-align: center;
        }

        label {
            display: block;
            margin: 10px 0 5px;
            font-weight: bold;
        }

        input {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #0056b3;
        }

        p {
            text-align: center;
            margin-top: 10px;
        }

        p span {
            color: #007bff;
            cursor: pointer;
            text-decoration: underline;
        }

        /* Close button */
        .close-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            font-size: 24px;
            cursor: pointer;
            color: #333;
        }

        .close-btn:hover {
            color: red;
        }
        input[type="text"],
input[type="password"],
input[type="email"],
input[type="date"] {
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 4px;
    width: 200px; /* Adjust the width to make the text box smaller */
}

input::placeholder {
    font-size: 16px; /* Adjust this value for the desired size */
}

input::placeholder {
    font-size: 16px; /* Medium font size */
    color: #888; /* Optional: change placeholder text color */
}
button[type="submit"],
button[type="Register"] {
    background-color: lawngreen;
    border: none;
    padding: 8px 15px; /* Adjusted padding */
    color: white;
    border-radius: 5px;
    cursor: pointer;
    font-size: 14px; 
    width: 200px; /* Set width to match the input fields */
}
/* Dropdown styles to match the navigation links */
.select-wrapper {
    position: relative;
    display: inline-block;
}

.dropdown {
    background-color: #333333;
    color: antiquewhite;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    font-size: large;
    padding: 15px 20px;
    border: none;
    cursor: pointer;
    width: auto; /* Make the dropdown width based on content */
    text-align: center;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease;
}



/* To make the options in the dropdown look better */
.dropdown option {
    background-color: #333333;
    color: antiquewhite;
    padding: 10px;
    font-size: large;
}

.dropdown option:hover {
    background-color: #555555;
}
/* Background overlay for blur effect */
.background-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent black */
    backdrop-filter: blur(8px); /* Blur effect */
    z-index: 2; /* Position above the page but below the form */
    display: none; /* Hidden by default */
}

/* Display the overlay when active */
.background-overlay.active {
    display: block;
}

/* Ensure form appears above the overlay */
.form-container {
    z-index: 3;
}

        
    </style>
    
 </head>
 <body>
   <div class="header">
        <div class="logo-container">
            <img src="360_F_169375330_ec1Xv9kLUPs9JxVwq9Fiq0QGpQQVZY24.jpg" alt="Logo" class="logo-image">
            <h1 style="color: blue;">Tecno<span style="color: #555555;">Zone</span></h1>
        </div>
    </div>

    <div class="topnav">
        <a href="#" style="font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif; font-size: large; background-color: #888;">HOME</a>
        <a href="lab7.html" style="font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif; font-size: large;">PRODUCTS</a>
        <a href="about.html" style="font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif; font-size: large;">ABOUT</a>
        <div class="select-wrapper">
            <select class="dropdown" onchange="window.location.href=this.value;">
                <option class="series-title" style="font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;" selected>SERIES</option>
                <option value="spark.html">Tecno Spark</option>
                <option value="camon.html">Tecno Camon</option>
                <option value="pova.html">Tecno Pova</option>
            </select>
        </div>
    </div>
    
    

    <!-- Open Login Label -->
    <a class="open-login" >
        <button onclick="showLogin()">Login</button>
    </a>
    
    <center>
    <div class="form-container" id="loginForm">
        <div class="close-btn" onclick="closeForm()">&times;</div>
        <h2>Login</h2>
        <form>
            <label for="username">Username</label>
            <input type="text" id="username" placeholder="Enter your username" required>

            <label for="password">Password</label>
            <input type="password" id="password" placeholder="Enter your password" required>

            <button type="submit">Login</button>
            <p>Don't have an account? <span onclick="showRegister()">Register here!</span></p>
        </form>
    </div>
    <div class="background-overlay" id="backgroundOverlay"></div>

    <!-- Login Form -->
    <div class="form-container" id="loginForm">
        <div class="close-btn" onclick="closeForm()">&times;</div>
        <h2>Login</h2>
        <form>
            <label for="username">Username</label>
            <input type="text" id="username" placeholder="Enter your username" required>
    
            <label for="password">Password</label>
            <input type="password" id="password" placeholder="Enter your password" required>
    
            <button type="submit">Login</button>
            <p>Don't have an account? <span onclick="showRegister()">Register here!</span></p>
        </form>
    </div>
    
    <!-- Register Form -->
    <div class="form-container" id="registerForm">
        <div class="close-btn" onclick="closeForm()">&times;</div>
        <h2>Register</h2>
        <form>
            <label for="email">Email Address</label>
            <input type="email" id="email" placeholder="Enter your email" required>
    
            <label for="firstName">First Name</label>
            <input type="text" id="firstName" placeholder="Enter your first name" required>
    
            <label for="lastName">Last Name</label>
            <input type="text" id="lastName" placeholder="Enter your last name" required>
    
            <label for="birthdate">Birthdate</label>
            <input type="date" id="birthdate" required>
    
            <label for="regUsername">Username</label>
            <input type="text" id="regUsername" placeholder="Choose a username" required>
    
            <label for="regPassword">Password</label>
            <input type="password" id="regPassword" placeholder="Create a password" required>
    
            <button type="submit">Save</button>
            <p>Already have an account? <span onclick="showLogin()">Log-in here!</span></p>
        </form>
    </div>
    

    <script>
        function showRegister() {
    document.getElementById('loginForm').classList.remove('active');
    document.getElementById('registerForm').classList.add('active');
    document.getElementById('backgroundOverlay').classList.add('active'); // Show overlay
}

function showLogin() {
    document.getElementById('registerForm').classList.remove('active');
    document.getElementById('loginForm').classList.add('active');
    document.getElementById('backgroundOverlay').classList.add('active'); // Show overlay
}

function closeForm() {
    document.getElementById('loginForm').classList.remove('active');
    document.getElementById('registerForm').classList.remove('active');
    document.getElementById('backgroundOverlay').classList.remove('active'); // Hide overlay
}

            </script>

    <div id="outerbox">
        <div id="slidebox">
            <img src="1.png">
            <img src="2.png">
            <img src="3.png">
            <img src="4.png">
            <img src="5.png">
            <img src="6.png">
            <img src="7.png">
            <img src="8.png">
            <img src="10.png">
            <img src="9.png">

            

        </div>
        
    
    </div>
    <div style="text-align: center; text-transform: uppercase; font-size: large; color: white; padding: 10px;font-family: Georgia, 'Times New Roman', Times, serif; background-color: #1a1d23;">LOOKING FOR AFFORDABLE PHONE OPTIONS?
        <br>HERE ARE SOME TOP PICKS!
    </div>
        <div class="thumbnail-gallery" style="margin-bottom: 20px;">
            <a href="22.html">
                <div class="thumbnail">
                <img src="22.png" alt="Thumbnail Tecno Pova 6 pro 5G">
                <div class="description"> Tecno Pova 6 pro 5G</div>
            </div></a>
            <a href="1.html">
              <div class="thumbnail">
                <img src="1.png" alt="Tecno Pova 3">
              <div class="description">Tecno Pova 3</div>
            
            </div></a>
            <a href="7.html"></a>
        
                <div class="thumbnail">
                  <img src="7.png" alt="Thumbnail Tecno Pova 5 X Free Fire">
                  <div class="description">Tecno Pova 5 X Free Fire</div>
            
            </div></a>
            <a href="11.html">
              <div class="thumbnail">
              <img src="11.png" alt="Thumbnail Tecno Pova neo 3">
              <div class="description">Tecno Pova neo 3</div>
            
            </div></a>
            <a href="29.html">
              <div class="thumbnail">
              <img src="29.png" alt="Thumbnail Tecno Pova 4 pro">
              <div class="description"> Tecno Pova 4 pro</div>
            </div></a></div>
    </div>

 </body>
 </html>
