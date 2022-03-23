<template>
<section>
  <div class="skewed bg-yellow-400"></div>
</section>
<div class="body ">
    <nav class="menu-container mt-12">
  <!-- burger menu -->
  <input type="checkbox" aria-label="Toggle menu" />
  <span></span>
  <span></span>
  <span></span>

  <!-- logo -->
  <a href="" class="menu-logo">
<h1 class=" text-2xl"> foodLink</h1>
    
  </a>

  <!-- menu items -->
  <div class="menu font-extrabold">
    <ul > 
      <li>
        <a href="#home">
          Home
        </a>
      </li>
      <li>
        <a href="#pricing">
          Pricing
        </a>
      </li>
      <li>
        <a href="#blog">
          about us
        </a>
      </li>
      <li>
        <a href="#docs">
          content us
        </a>
      </li>
    </ul>
    <ul>
      <li>
        <a href="#signup">
          Sign-up
        </a>
      </li>
      <li>
        <a href="#login">
          Login
        </a>
      </li>
    </ul>
  </div>
</nav>
</div>
<div class=" grid grid-cols-2 absolute  ">
<div class=" mt-24 ml-4  space-y-9"><h1 class=" text-6xl font-bold">Your 
<span class=" text-amber-400 mt-2 ">favorite's </span>
Food
Delivered Hot &
Fresh</h1> 
<h3 class=" text-3xl font-semibold "> Healthy switcheroos de of the prep work, the prepping
chopping & marinoting, so you can cook fresh food</h3>
<button class=" bg-yellow-400 text-xl font-bold ml-40">Order Now</button>
</div>
<div class="img ">
<img src="../assets/0.jpeg" alt="" class=" rounded-full">
</div>
</div>
<div > 
<img src="../assets/1.png"  class="w-52 p-5  absolute bottom-0    rounded-full">
</div>
</template>
<style scoped>

button {
 width: 9em;
 height: 3em;
 border-radius: 30em;

 border: none;
 position: relative;
 overflow: hidden;
 z-index: 1;
 box-shadow: 6px 6px 12px #c5c5c5,
             -6px -6px 12px #111110;
}

button::before {
 content: '';
 width: 0;
 height: 3em;
 border-radius: 30em;
 position: absolute;
 top: 0;
 left: 0;
 background-image: linear-gradient(to right, #0fd850 0%, #f9f047 100%);
 transition: .5s ease;
 display: block;
 z-index: -1;
}

button:hover::before {
 width: 9em;
}
.img {
    height: 500px;
    width: 500px;
border-radius: 50%;
background: linear-gradient(-145deg, #0c0c0c, #111111);
box-shadow:  50px 50px 100px #eeeaea,
             -50px 50px 100px #0a0a0a;
    }
.skewed {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  width: 100%;
  height: 100%;
 
  z-index: 0;
  transform: skewY(35deg);
  transform-origin: top right;
}

.menu-container {
  position: relative;
  display: flex;
  align-items: center;
  margin-bottom: 20px;

  color: #0b0b0b;
  padding: 20px;
  z-index: 1;
  -webkit-user-select: none;
  user-select: none;
  box-sizing: border-box;
}

.menu-logo {
  line-height: 0;
  margin: 0 20px;
}

.menu-logo img {
  max-height: 40px;
  max-width: 100px;
  flex-shrink: 0;
}

.menu-container a {
  text-decoration: none;
  color: #edede6;
  transition: color 0.3s ease;
}

.menu-container a:hover {
  color: #0aefcb;
}

.menu-container input {
  display: block;
  width: 50px;
  height: 25px;
  margin: 0;
  position: absolute;
  cursor: pointer;
  opacity: 0; /* hide this */
  z-index: 2; /* and place it over the hamburger */
  -webkit-touch-callout: none;
}

/* Burger menu */
.menu-container span {
  display: block;
  width: 33px;
  height: 4px;
  margin-bottom: 5px;
  position: relative;
  background: #f00505;
  border-radius: 3px;
  z-index: 1;
  transform-origin: 4px 0px;
  transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
              background 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
              opacity 0.55s ease;
}

.menu-container span:first-child {
  transform-origin: 0% 0%;
}

.menu-container span:nth-child(3) {
  transform-origin: 0% 100%;
}

.menu-container input:checked ~ span {
  opacity: 1;
  transform: rotate(45deg) translate(3px,-1px);
  background: #edede6;
}

.menu-container input:checked ~ span:nth-child(4) {
  opacity: 0;
  transform: rotate(0deg) scale(0.2, 0.2);
}

.menu-container input:checked ~ span:nth-child(3) {
  transform: rotate(-45deg) translate(-5px,11px);
}

.menu ul {
  list-style: none;
}

.menu li {
  padding: 10px 0;
  font-size: 30px;
}

/* mobile styles */
@media only screen and (max-width: 830px) { 
  .menu-container {
    flex-direction: column;
    align-items: flex-end;
  }
  
  .menu-logo {
    position: absolute;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
  }

  .menu-logo img {
    max-height: 30px;
  }

  .menu {
    position: absolute;
    box-sizing: border-box;
    width: 300px;
 
    right: -300px;
    top: 0;
    margin: -20px;
    padding: 75px 50px 50px;
    background: #e40505;
    -webkit-font-smoothing: antialiased;
    /* to stop flickering of text in safari */
    transform-origin: 0% 0%;
    transform: translateX(0%);
    transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0);
  }

  .menu-container input:checked ~ .menu {
    transform: translateX(-100%);
  }
}

/* desktop styles */
@media only screen and (min-width: 831px) { 
  .menu-container {
    width: 100%;
  }

  .menu-container a {
    color: #0b0b0b;
  }

  .menu-container input {
    display: none;
  }

  /* Burger menu */
  .menu-container span {
    display: none;
  }

  .menu {
    position: relative;
    width: 100%;
    display: flex;
    justify-content: space-between;
  }

  .menu ul {
    display: flex;
    padding: 0;
  }

  .menu li {
    padding: 0 20px;
  }
}
</style>