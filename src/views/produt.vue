<template>
  <div class="about">
  <div class="cater3-movingBG">
<div class="flyinTxtCont">
<div class="flyIn lineOne">Fiestas</div>
<div class="flyIn lineTwo">Without </div>
<div class="flyIn lineThree">the fuss</div>
  <div class="flyIn lineFour">Catering. Delivered. Set up. Delicious.</div>
</div>
</div>
  </div>
</template>

<style scoped>
.about {
  background:#000;
}
.cater3-movingBG {
    height: 100%;
    background-image: url(http://salsaritas.johngroupinteractive.com/wp-content/uploads/2017/06/enchilada-bg.jpg);
    background-size: 125%;
    background-repeat: repeat-x;
    animation: animatedBackground 15s linear alternate infinite;
}

@keyframes animatedBackground {
    0% { background-position: 0 0; }
    50% { background-position: 50% 0; }
    100% { background-position: 0 0; }
}

.flyinTxtCont {
    height: 100%;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    -webkit-box-align: start;
    -ms-flex-align: start;
    align-items: flex-start;
    -webkit-box-pack: end;
    -ms-flex-pack: end;
    justify-content: flex-end;
    padding-bottom: 10%;
      margin-left: 2em;
}
.flyIn {
    color:#fff;
    font-family:'Raleway';
    text-transform:uppercase;
    line-height:1.2em;
    position:relative;
  text-shadow: 2px 2px 40px rgba(0,0,0,0.7);
}
.lineOne {
  transition-delay:.2s; 
  transition:.4s ease in;
  animation: txtFlyIn .3s linear;
}
.lineTwo {
    transition-delay:.4s; 
    transition:.6s ease in;
    animation: txtFlyIn .6s linear;
}
.lineThree {
    transition-delay:.6s; 
    transition:.8s ease in;
    animation: txtFlyIn .9s linear;
}
.lineOne, .lineTwo, .lineThree {
    font-size:110px;
    font-weight: bold;
    letter-spacing: 3px;
  }
.lineFour {
    transition-delay:2s; 
    transition:2s ease in;
    animation: fadeIn 2s linear;
    width: 100%;
    background-color:rgba(255,255,255,0.9);
    display:inline-block;
    color:#000;
    box-size:border-box;
    max-width:63%;
    max-width: 22em;
    font-size: 32px;
    padding: .2em .5em;
    margin-top: 30px;
}
@keyframes fadeIn{
    0% { opacity:0;}
    100% { opacity:1;}
}
@keyframes txtFlyIn{
    0% { transform:translateX(-100%); }
    100% { transform:translateX(0%); }
}
</style>
