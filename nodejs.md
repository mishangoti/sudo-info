#### MVC application structure    
> **App_Data:** All the data which is required for read & write into application.   
> **App_Start:** Here you put all the configuration file. Ex - Route configuration, budle configuration, etc.   
> **Content:** It stores Images, CSS etc. (Other than scripts)    
> **Controllers:** Here you put all the controllers   
> **Fonts:** These are some custom fonts which are used by Bootstrap.    
> **Models:** This folder has all the models   
> **Scripts:** Here you put all the scripts of the application   
> **Views:**  Here you put all the views (html code 😊)    
> **Favicon.ico:**   favicon file  
> **packages.config:**   All the installed packages are available here   (same as package.json)   
> **We.config:**  Configuration file   
> 

#### Role of a controller   
 - Work with user input (or browser request)   
 - Play an important role in flow of application by handling incoming request and provide data to corresponding view or to browser request   

_Controllers are .cs files which reside in Controllers folder. Controllers are used to handle browser incoming http request, get data from models (if required), provide data to corresponding view or request(directly) and generate response._   

> **What are action methods?**   
> - A method inside a Controller is called as Action Method   
> - Default return type of an Action method is ActionResult    
> - Only a public method can access from http request   
> - By default all Action methods are GET   
> - An action method can return View, File, Partial View, JSON, string, etc.   

 > **Make call from a browser**
 > YourDomain/ControllerName/ActionMethodName   
 > e.g., localhost:xxxx/Home/Index    
 > Make sure you don't write whole controller name i.e., HomeController    
 
> * Params in Action Method   
> Localhost:xxxx/Employee/Profile?id=1    
> Localhost:xxxx/Employee/Address?id=1&Department=tech   
> **Note:** _To use more than one string parameters we need to use & operator_    
> **Nullable parameters:**  There are some parameters those are optional and if the type of such parameter is int then we need to make it nullable parameter otherwise it will throw an error while user don't pass any value to that param.   
> syntax   
> ```c#     
>       using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.Mvc;

namespace WebApplication2.Controllers
{
    public class EmployeeController : Controller
    {
        public string Address(int id, int? code = null)
        {
            return "id = " + id + "dept = " + code;  
        }
    }
}  
> ```   
> So. in the above code snippet, code parameter is nullable param. so we need to insert a ? after data type and have to provide a default value to it    


#### What is a view?   
> - One of main pillar of MVC (V - view)  
> - .cshtml file (c sharp + html)  
> - UI of application  
> - Support pure HTML   
> - Everything which is visible to a user on browser is view   

> **Why view is required?**   
> - To make your application interactive   
> - Easy to use   
> - To use html and other client side framework   

> **Adding a new view**   
> - view can be added for an action method     
> - can be added using solution explorer.     
> - also by using action method    
> - Acttion method return type must be ViewResult or ActionResult   

> **Calling a view from browser**    
> - In MVC **browser cannot directly call a view**    
> - Every call must go through controller   
> - Browser don't even know whether it is calling a View or something else because its a job of action method. If action is returning a view then browser will display the content.   

> **How controller find a view?**   
> - First it searches in corresponding view folder (Same name as controller)   
> - Then goes to Share folder   
> - If view file's name is different than controller's name, then we have to specify the specific name of the view   
> ```c#    
>    /*some code here*/     
>     public ActionResult Index(){   
>       return View("NewViewName");
>     }      
>    /*some code here*/     
> ```     
