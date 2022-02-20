# Design a Website for Server Side Processing

## AIM:
To design a website to perform mathematical calculations in server side.

## DESIGN STEPS:

### Step 1:
crate a django project




### Step 2:
create a app named max app




### Step 3:
in max app create a folder name template



### Step 4:
create a hrml document in mat app



### Step 5:
the html document design the page as required for getting the input valuesfor doing maths calculation



### Step 6:
add formula in the views .py.


### Step 7:
Link the html document to urls.py



## PROGRAM :
~~~

<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <title>Area</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <style>
        body{
            text-align: center;
            background-color: aqua;
        }
        .maindiv{
            margin-left:400px;
              text-align: center;
            border-style: dashed;
            width: 550px;
            height: 300px;
            background-color: aquamarine;
        }
        h1{
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <h1>Server Side processing</h1>
    
    <div class="maindiv">
        <h1>Area of Rectangle</h1>
        <form method="POST">
            {% csrf_token %}
            Length = <input type="text" name="length" value="{{l}}"> meters <br/>
            <br/>
            width = <input type="text" name="width" value="{{w}}"> meters<br/>
            <br/>
            <input type="submit" value="Calculate"><br/>
            <br>
            Area = <input type="text" name="area" value="{{area}}"> meter<sup>2 </sup><br/>
        </form>
        <br>
        <br>
        <footer>
            Developed by:challa sandeep
        </footer>
    </div>
</body>
</html>
views.py
from django.shortcuts import render

def areacalculation(request):
    context = {}
    context["area"] = "0"
    context["l"] = "0"
    context["w"] = "0"
    if request.method == "POST":
        b = request.POST.get("length","0")
        h = request.POST.get("width","0")
        area = (int(l) * int(hw)
        context["area"] = area
        context["l"] = l
        context["w"] = w
    return render(request,"mathapp/area.html",context)
urls.py
from django.contrib import admin
from django.urls import path
from mathapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path("areaofrectangle/",views.areacalcul
    ation,name="areaofrectangle"),
    path("",views.areacalculation,name="areaofrectangleroot")
]
~~~
## OUTPUT:
![WhatsApp Image 2022-02-20 at 09 28 56](https://user-images.githubusercontent.com/93427522/154828059-93211c2d-6406-47f5-b813-e381792e30bf.jpeg)


## Result:
Therefor the above codes are successfully executed to run server side programming and mathematical calcualtions.

