# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include regularexpression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mathematical Calculations</title>
    <style>
    * {
      box-sizing: border-box;
      font-family: Arial, Helvetica, sans-serif;
    }
    body {
      background-color: #000000;
      background-image: linear-gradient(147deg,#000000 0%,#04619f 74%);
    }
    .container {
      width: 1080px;
      margin-left: auto;
      margin-right: auto;
    }
    .content {
      display: block;
      width: 100%;
      background-color: #93A5CF;
      background-image: linear-gradient(147deg,#93A5CF 0%,#E4EfE9 74%);
      min-height: 500px;
      margin-top: 150px;
      margin-bottom: 150px;
    }
    .content2{
      display: block;
      width: 100%;
      background-color: #93A5CF;
      background-image: linear-gradient(147deg,#93A5CF 0%,#E4EfE9 74%);
      min-height: 500px;
      margin-top: 150px;
      margin-bottom: 150px;
    }
    h1{
      text-align: center;
      font-size:XX-large;
      padding-top: 50px;
      padding-bottom: 20px;
      color: white;
    }
    h2{
      text-align: center;
      font-size:XX-large;
      padding-top: 50px;
      padding-bottom: 20px;
      color: black;
    }
    .formelement{
      text-align: center;
      font-size:X-large;
      margin-top: 5px;
      margin-bottom: 5px;
    }
    .footer{
      display: block;
    width: 100%;
    height: 45px;
    background-color: #084475;
    text-align: center;
    font-size: x-large;
    padding-top: 10px;
    margin: 0px 0px 0px 0px;
    color: whitesmoke;
    }
    </style>
  </head>
  <body>
    <h1><u> WEBPAGE FOR MATHEMATICAL CALCULATIONS </u></h1>
    <div class="container">
      <div class="content">
          <h2><u>AREA OF TRAPEZOID</u></h2>
          <form>
              <div class=formelement>
                  <label for="aedit">Base-1:</label>
                  <input type="text" id="aedit" value=""/>
                  <label for="aedit">cm</label>
              </div><br>
              <div class=formelement>
                  <label for="bedit">Base-2:</label>
                  <input type="text" id="bedit" value=""/>
                  <label for="bedit">cm</label>
              </div><br>
              <div class=formelement>
                  <label for="cedit">Height:</label>
                  <input type="text" id="cedit" value=""/>
                  <label for="bedit">cm</label>
              </div><br>
              <div class=formelement>
                  <input type="button" value="CALCULATE AREA" id="xbutton"/>
              </div><br>
              <div class=formelement>
                  <label for="dedit">Area:</label>
                  <input type="text" id="dedit" readonly=""/>
                  <label for="dedit">sq.cm</label>
              </div><br>
              <div class=formelement>
                <u>Formula</u> : Area of a TRAPEZOID = base(1+2)*height/2
              </div>
          </form>
      </div>
      <script type="text/javascript">
          var button;
          button=document.querySelector("#xbutton");
          button.addEventListener("click",function()
          {
          var atext,btext,ctext,dtext;
          var aval,bval,cval,dval;
          atext=document.querySelector("#aedit");
          btext=document.querySelector("#bedit");
          ctext=document.querySelector("#cedit");
          dtext=document.querySelector("#dedit");

              aval=parseInt(atext.value);
              bval=parseInt(btext.value);
              cval=parseInt(ctext.value);
              dval=(aval+bval)*cval/2;
              dtext.value=""+dval;
              res=dtext.value;
              if (res=="NaN")
              {
                alert("Please Enter Integers");
              }
          });
      </script>
      <div class="content2">
          <h2><u>VOLUME OF TRIANGLE</u></h2>
          <form>
              <div class="formelement">
                <lable for="ledit">Breadth:</lable>
                <input type="text" id="ledit" value=" "/>
                <label for="ledit">cm</label>
              </div><br>
              <div class="formelement">
                <lable for="medit">Height:</lable>
                <input type="text" id="medit" value=" "/>
                <label for="medit">cm</label>
              </div><br>
              <div class="formelement">
                <lable for="nedit">Length:</lable>
                <input type="text" id="nedit" value=" "/>
                <label for="nedit">cm</label>
              </div><br>
              <div class="formelement">
                <input type="button" value="CALCULATE VOLUME" id="ybutton"/>
              </div><br>
              <div class="formelement">
                <lable for="oedit">Volume:</lable>
                <input type="text" id="oedit" readonly=""/>
                <label for="oedit">cm³</label>
              </div><br>
              <div class="formelement">
              <u>Formula</u> : Volume of a Triangle = 0.5*Breadth*Height*Length
              </div><br>
              
          </form>
  
          </div>
      </div>
      <script type="text/javascript">
        var button;
        button=document.querySelector("#ybutton");
        button.addEventListener("click",function()
           {
            var ltext,mtext,ntext,otext;
            var lval,mval,nval,oval;
  
            ltext=document.querySelector("#ledit");
            mtext=document.querySelector("#medit");
            ntext=document.querySelector("#nedit");
            otext=document.querySelector("#oedit");
    
            lval=parseInt(ltext.value);
            mval=parseInt(mtext.value);
            nval=parseInt(ntext.value);
            oval=0.5*lval*mval*nval;
            otext.value=""+oval;
            res1=otext.value
            if (res1=="NaN")
            {
              alert("Please Enter Integers");
            }
          });
      </script> 
    <div class="footer">
       Developed by SARAVANA KUMAR.S
    </div>     
  </body>
</html> 
```
## OUTPUT:

![output](./calculations/img/output.png)

## Result:

Thus a website is designed to perform mathematical calculations in the client side.
