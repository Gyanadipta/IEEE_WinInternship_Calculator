<script lang="javascript">
    function calculateAge() {
      // let dob = document.getElementById("user-dob").value;
      // console.log(dob);
    }
      let navbutton = document.querySelector("navbarmenuicon");
      let sidebar = document.querySelector(".sidebar");
      let searchBtn = document.querySelector("bx-search-alt-2");
      // navbutton:onclick = function navbar() {
      //   sidebar.classList.toggle("active");
      // }
  </script>
  
  
  <main>
    <div class="sidebar">
      <div class="logo-content">
        <div class="logo">
          <i class='bx bx-calculator' ></i>
          <div class="logo-name">Calculator</div>
        </div>
        <i class='bx bx-menu' id="navbarmenuicon"></i>
      </div>
      <ul class="nav-list">
        <li>
            <i class='bx bx-search-alt-2' ></i>
            <input type="text" placeholder="Search...">
          <span class="tooltip">Search</span>
        </li>
  
        <li>
          <a href="somelink.svelte">
            <i class='bx bx-home-alt-2' ></i>
            <span class="links-name">Home</span>
          </a>
          <span class="tooltip">Home</span>
        </li>
  
        <li>
          <a href="somelink.svelte">
            <i class='bx bxs-group' ></i>
            <span class="links-name">About</span>
          </a>
          <span class="tooltip">About</span>
        </li>
  
        <li>
          <a href="somelink.svelte">
            <i class='bx bx-question-mark' ></i>
            <span class="links-name">How to Use</span>
          </a>
          <span class="tooltip">How to Use</span>
        </li>
  
        <li>
          <a href="somelink.svelte">
            <i class='bx bx-category' ></i>
            <span class="links-name">Some Other Option</span>
          </a>
          <span class="tooltip">Some Other Option</span>
        </li>
      </ul>
    </div>
  
  
  <head>
    <link href='https://fonts.googleapis.com/css?family=Inter' rel='stylesheet'>
    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
  </head>
    <div class="header">
      <img src="images/calculator-icon.png" alt="Logo" class="header-img"/>
      <p class="header-text">Calculator</p>
    </div>
  
    <div class="card">
     <!-- background of calculator -->
    </div>
    <div class="div-head">
      <p class="calc-heading">
        Age Calculator
      </p>
    </div>
    <div class="dob">
  
      <p class="dob-text">Date of Birth:</p>
      <input type="date" class="dob-input" id="user-dob"/>
  
      <p class="crdt-text">Current Date:</p>
      <input type="date" class="curr-input" id="current-date"/>
  
    </div>
    <button class="calculate-btn" on:click={calculateAge}>Calculate</button>
    <hr class="solid"/>
    <p class="output-text">Your age is:</p>
  
  </main>
  
  
  <style>
  
    .sidebar {
      top: 100px;
      left: 0;
      position: fixed;
      height: 100%;
      width: 240px;
      background: #28282B;
  
      padding: 6px 14px;
  
    }
  
    .sidebar .logo-content .logo {
      color: #fff;
      display: flex;
      height: 50px;
      width: 100%;
      align-items: center;
    }
  
    .logo-content .logo i {
      font-size: 35px;
      margin-right: 5px;
    }
  
    .logo-content .logo .logo-name {
      font-size: 20px;
      font-weight: 400;
    }
  
    .sidebar #navbarmenuicon {
      position: absolute;
      color: #FFF;
      left: 90%;
      top: 25px;
      font-size: 20px;
      height: 50px;
      width: 50px;
      text-align: center;
      line-height: 50px;
      transform: translateX(-50%);
    }
  
    .sidebar ul {
      margin-top: 20px;
      padding-inline-start: 0;
      margin-block-end: 0;
    }
  
    .sidebar ul li {
      position: relative;
      height: 50px;
      width: 100%;
      list-style: none;
      line-height: 50px;
      border-radius: 12px;
    }
  
    .sidebar ul li .tooltip {
      position: absolute;
      left: 122px;
      top: 0%;
      transform: translateY(-50%);
      border-radius: 6px;
      height: 35px;
      width: 122px;
      line-height: 35px;
      text-align: center;
      background: #FFF;
      box-shadow: 0 5px 10px rgba(0, 0, 0,0.2);
      transition: 0s;
      opacity: 0;
      pointer-events: none;
    }
  
    .sidebar ul li:hover .tooltip {
      transition: all 0.5s ease;
      opacity: 1;
      top: 50%;
    }
  
  
    .sidebar ul li input {
      position: absolute;
      height: 100%;
      left: 0;
      top: 0;
      border-radius: 12px;
      outline: none;
      border: none;
      background: #F7F7F8;
      padding-left: 50px;
      font-size: 18px;
      color: rgb(0, 0, 0);
    }
  
    .sidebar ul li .bx-search-alt-2 {
      position: absolute;
      z-index: 99;
      font-size: 22px;
  
    }
  
    .sidebar ul li a {
      color: #fff;
      display: flex;
      align-items: center;
      text-decoration: none;
      transition: all 0.4s ease; 
      border-radius: 12px;
    }
  
    .sidebar ul li a:hover{
      color: #28282B;
      background: #FFF;
    } 
    
    .sidebar ul li i {
      height: 50px;
      min-width: 50px;
      border-radius: 12px;
      line-height: 50px;
      text-align: center;
    }
  
    main {
      position: fixed;
      font-family: 'Inter';
      min-height: 100vh;
      width: 100%;
      margin: 0 5px;
      overflow: hidden;
    }
   
    .header {
  
      display: flex;
      align-items: center;
  
      position: fixed;
      width: 100%;
      height: 115px;
      left: 0px;
      top: 0px;
  
    background: #28282B;
    }
  
    .header-img {
      position: absolute;
      width: 54px;
      height: 54px;
      left: 80px;
      top: 30px;
  
    }
  
    .header-text {
      position: absolute;
      width: 203px;
      height: 48px;
      left: 152px;
  
      font-family: 'Inter';
      font-style: normal;
      font-weight: 600;
      font-size: 40px;
      line-height: 48px;
      letter-spacing: 0.4px;
  
      color: #FFFFFF;
  
    }
  
   .card {
    position: absolute;
    width: 413px;
    height: 652px;
    left: calc(50% - 413px/2 + 402.5px);
    top: 171px;
  
    background: #F7F7F8;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 16px;
   }
  
   .div-head {
  
    /* Added the 3 lines to make the text on top of this card centered */
      display: flex;
      align-items: center;
      justify-content: center;
  
    position: absolute;
    width: 413px;
    height: 122px;
    left: calc(50% - 413px/2 + 402.5px);
    top: 171px;
  
    background: #005DE2;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 5px;
   }
  
   .calc-heading {
  
    position: relative;
    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 32px;
    color: #FFFFFF;
   }
  
   .dob-text {
    position: absolute;
    width: 99px;
    height: 19px;
    left: calc(50% - 99px/2 + 288.5px);
    top: 334px;
  
    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 19px;
    letter-spacing: -0.32px;
  
    color: #000000;
  
   }
  
   .crdt-text {
    position: absolute;
    width: 101px;
    height: 19px;
    left: calc(50% - 101px/2 + 288.5px);
    top: 470px;
  
    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 19px;
    letter-spacing: -0.32px;
  
    color: #000000;
  
   }
  
  hr {
    position: absolute;
    width: 414px;
    height: 0px;
    left: calc(50% - 414px/2 + 403px);
    top: 717px;
  
    border: 1px solid rgba(153, 153, 154);
  }
  
  .calculate-btn {
    box-sizing: border-box;
  
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px 14px;
    gap: 8px;
  
    position: absolute;
    width: 100px;
    height: 36px;
    left: calc(50% - 100px/2 + 404px);
    top: 627px;
  
    background: #0066FF;
    border: 1px solid #0066FF;
    border-radius: 8px;
  
    color: #FFFFFF;
  }
  
  .dob-input {
    box-sizing: border-box;
  
    /* Auto layout */
  
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 10px 14px;
    gap: 8px;
  
    position: absolute;
    width: 207px;
    height: 44px;
    left: calc(50% - 207px/2 + 421.5px);
    top: 379px;
  
    /* White */
  
    background: #FFFFFF;
    /* Gray/300 */
  
    border: 1px solid #D0D5DD;
    /* Shadow/xs */
  
    box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
    border-radius: 8px;
    }
  
  .curr-input {
    box-sizing: border-box;
  
    /* Auto layout */
  
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 10px 14px;
    gap: 8px;
  
    position: absolute;
    width: 207px;
    height: 44px;
    left: calc(50% - 207px/2 + 421.5px);
    top: 527px;
  
    /* White */
  
    background: #FFFFFF;
    /* Gray/300 */
  
    border: 1px solid #D0D5DD;
    /* Shadow/xs */
  
    box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
    border-radius: 8px;
  }
  
  .output-text {
    
    position: absolute;
    width: 86px;
    height: 19px;
    left: calc(50% - 86px/2 + 282px);
    top: 760px;
  
    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 19px;
    letter-spacing: -0.32px;
  
    color: #000000;
  }
  
  </style>