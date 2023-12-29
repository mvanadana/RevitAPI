# Adding a Panel in Revit Using Revit API
## Overview
This instruction file outlines the steps to add a custom panel with a "Hello World" button to the Revit user interface using the Revit API.

## Steps
1. Setting Up the Project
Create a new Class Library project in Visual Studio for your Revit API application.
Add references to Autodesk.Revit.DB and Autodesk.Revit.UI assemblies.
2. Implementing the Add-in Classes
Copy and paste the provided code into your project.
Ensure the namespaces and class names align with your project structure.
3. Adding the Panel and Button
In the CsAddPanel class:
Modify the panel name in RibbonPanel ribbonPanel = application.CreateRibbonPanel("NewRibbonPanel"); to suit your panel's name.
Customize the button label and functionality in PushButtonData constructor: PushButtonData("cmdHelloWorld", "Hello World", thisAssemblyPath, "Walkthrough.HelloWorld");
Assign a tooltip and a large bitmap to the button for better user experience.
4. Adjusting Image Path (Optional)
Update the image path in Uri uriImage = new Uri(@"C:\Path\To\Your\Image.png"); to the location of your desired image for the button.
5. Building and Deploying
Build the solution to generate the DLL file.
Place the compiled DLL into the appropriate Revit Addins folder:
For example, C:\ProgramData\Autodesk\Revit\Addins\<YourRevitVersion>.
6. Loading the Add-in in Revit
Open Revit and navigate to the Add-ins tab.
Look for your custom panel with the "Hello World" button in the specified location.
Click the button to execute the command and display the "Hello World" message using a TaskDialog.

![Screenshot (180)](https://github.com/mvanadana/RevitAPI/assets/149364066/15fad8b7-fc69-4463-a627-937ca500aff5)

## Conclusion
By following these steps, you'll successfully add a custom panel and a button in Revit, triggering a "Hello World" message upon clicking the button. Customize the panel, button behavior, and appearance as needed for your specific application.
