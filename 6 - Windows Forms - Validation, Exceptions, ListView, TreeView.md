# Windows Forms – Validation, Exceptions, ListView, TreeView

##	 Contents

1. [Data Validation](#data-validation)
2. [Complex Visualization Controls](#complex-visualization)
	1. [ListView](#listview)
	2. [TreeView](#treeview)
3. [Exception Handling](#exception-handling)
	1. [Custom Exceptions](#custom-exceptions)
	2. [Standard Exceptions](#standard-exceptions)

## <a name="data-validation"></a>Data Validation

**Assignment**

![C#](https://raw.githubusercontent.com/cristianfrasineanu/ase-windows-applications-programming/master/media/image1.png) Sample Code available at <http://online.ase.ro> – “ValidationCustomExceptions” Sample

1. Create a new project with the name “ValidationCustomExceptions”
![UI Preview](https://raw.githubusercontent.com/cristianfrasineanu/ase-windows-applications-programming/master/docs/6/ui-preview.png)
3. Add ErrorProviders for the LastName and FirstName fields: **epLastName**, **epFirstName**
4. Handle the **Validating** event on **tbLastName** as follows:

	```c#
	string lastName = ((TextBox) sender).Text.Trim();
	}
	```
5. Handle the **Validated** event on **tbLastName** as follows:

	```c#
	epLastName.Clear();
	```
6.	Handle the **Validating** and **Validated** events for the **tbFirstName** in a similar manner
7. 	Handle the **Click** event on the “Add Participant” button as follows
	private void btnAdd_Click(object sender, EventArgs e)
	```
8.	Why is it recommended to have the validations both on the individual controls and in the handler for the “Add Participant” button?

## <a name="complex-visualization"></a>Complex Visualization Controls

### <a name="listview"></a> ListView

**Assignment**

![C#](https://raw.githubusercontent.com/cristianfrasineanu/ase-windows-applications-programming/master/media/image1.png) Sample Code available at <http://online.ase.ro> – “ListViewSample” Sample

1. Create a new project with the name “ListViewSample”
2. Rename “Form1” to “MainForm”
3. Create the following UI:    
![Browser App Preview](https://raw.githubusercontent.com/cristianfrasineanu/ase-windows-applications-programming/master/docs/6/listview-ui.png)
4. Add a new folder to your project and name it “Entities”
5. Inside the “Entities” folder add the following “Participant” class:

	```c#
	internal class Participant
	```
6. Final form of the “MainForm” class
	
	```c#
	public partial class MainForm : Form
	}
	```
7. Add buttons for changing the current “View” of the list, as shown:  
![Grouped ListView](https://raw.githubusercontent.com/cristianfrasineanu/ase-windows-applications-programming/master/docs/6/grouped-list.png)
8. Display the participants in groups (“Children” and “Adults”) as in the previous image
### <a name="treeview"></a> TreeView

**Assignment**

![C#](https://raw.githubusercontent.com/cristianfrasineanu/ase-windows-applications-programming/master/media/image1.png) Sample Code available at <http://online.ase.ro> – “TreeViewSample” Sample

1. Create a new project with the name “TreeViewSample”
2. Create the following UI:  
![TreeView UI](https://raw.githubusercontent.com/cristianfrasineanu/ase-windows-applications-programming/master/docs/6/treeview-ui.png)
3. Add the following methods:

	```c#
	 #region Methods
	```

## <a name="exception-handling"></a> Exception Handling

### <a name="custom-exceptions"></a> Custom Exceptions

**Assignment**

1. Add the following “InvalidBirthDateException” class:

	```c#
	public class InvalidBirthDateException : Exception
	```
2. Update the “BirthDate” property in the “Participant” class in order to validate the received value:

	```c#
	#region BirthDate
	```
3. Update the event handler for the “Add Participant” button in order to handle the potential exceptions:

	```c#
	try
	```

### <a name="standard-exceptions"></a> Standard Exceptions

* common exception types: System.NotImplementedException, [System.DivideByZeroException](https://msdn.microsoft.com/en-us/library/system.dividebyzeroexception%28v=vs.110%29.aspx), System. FormatException

![Info](https://raw.githubusercontent.com/cristianfrasineanu/ase-windows-applications-programming/master/media/image3.png) Further reading: [link](https://msdn.microsoft.com/en-us/library/ms173160.aspx)

**Assignment**

1. Create a new project with the name “StandardExceptions”
2. Create the following UI:  
![Standard Exceptions](https://raw.githubusercontent.com/cristianfrasineanu/ase-windows-applications-programming/master/docs/6/standard-exceptions-example.png)
3. Handle the possible exceptions

	```c#
	 try
	```

	```c#
	static class Program
	```