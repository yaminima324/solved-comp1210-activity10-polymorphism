Download Link: https://assignmentchef.com/product/solved-comp1210-activity10-polymorphism
<br>
By the end of this project you should:

<ul>

 <li>Have an understanding of polymorphism via inheritance</li>

 <li>Be able to create methods that use polymorphism to deal with multiple types of objects <strong>Directions: </strong></li>

</ul>

Don’t forget to add your Javadoc comments for your classes, constructor, and methods in this activity.




For this assignment, you will need <u>your classes from Activity on “Inheritance”</u> except for the driver program. If you haven’t created these classes, you’ll need to do them as part of this activity.




<h1>ItemsList</h1>

<ul>

 <li>Create a <u>class called ItemsList</u>. This class will hold an array of InventoryItem objects (which includes objects of subclasses of InventoryItem; recall an instance of a subclass of InventoryItem <em>is an</em> InventoryItem).</li>

</ul>




<ul>

 <li>Declare an <u>instance variable</u> in your class of type InventoryItem array which is called inventory and an int called count to track the number items in inventory.</li>

</ul>




private _________[] inventory; private _____ count;




<ul>

 <li>Create a <u>constructor</u> for ItemsList that has no parameters. Add the following code to instantiate the InventoryItem array.</li>

</ul>




_____ = new InventoryItem[20]; count = ____;




<ul>

 <li>Create the following method stubs for your class:</li>

</ul>

o addItem: with parameter InventoryItem itemIn; no return. o calculateTotal: with parameter double electronicsSurcharge; double return.




<ul>

 <li>The addItem method takes an InventoryItem as a parameter, assigns it to the element at positon count in the inventory array, and then increments count. No need to worry about exceeding the capacity of the array in this activity.</li>

</ul>




<ul>

 <li>Create a toString method in ItemsList. The toString method should iterate through inventory from 0 up to count (but not including count) to append the toString for each item to output:</li>

</ul>







Recall, the Object class has a toString method, which is inherited by its subclasses. When you define a toString method in your class, you are overriding an inherited toString method.

<h1>InventoryListApp – driver class and main method</h1>

<ul>

 <li>Create a class called InventoryListApp and add a main method. In the main method, instantiate a ItemsList object called myItems.</li>

</ul>




<ul>

 <li>In the main method, set the tax rate to 0.05 by invoking the InventoryItem.setTaxRate method.</li>

</ul>




<ul>

 <li>Instantiate the following 4 items in the main method and add them to myItems:</li>

</ul>

o ElectronicsItem: name = “laptop”, price = $1234.56, weight = 10 lbs

myItems._____(new ElectronicsItem(_____, 1234.56, 10));

o InventoryItem: price = $9.8, name = “motor oil” o OnlineBook: price = $12.3, name = “All Things Java” o OnlineArticle: price = $3.4, name = “Useful Acronyms”

<ul>

 <li>Print the toString return value of the ItemsList object myItems to standard output:</li>

</ul>

<table width="559">

 <tbody>

  <tr>

   <td width="559">ÏÏ«Ï —-jGRASP exec: java -ea InventoryListApp ÏÏ§Ï ÏÏ§ÏAll inventory: ÏÏ§ÏÏÏ§Ïlaptop: $1311.288ÏÏ§Ïmotor oil: $10.290000000000001ÏÏ§ÏAll Things Java – Author Not Listed: $12.3ÏÏ§ÏUseful Acronyms: $3.4 ÏÏ§ÏÏÏ©Ï —-jGRASP: operation complete. </td>

  </tr>

 </tbody>

</table>




<h1>ItemsList: calculateTotal</h1>

<ul>

 <li>The calculateTotal method in ItemsList accepts surcharge for electronics items as a parameter and returns the total price of all of the items. You’ll have to iterate through each of the items in inventory and add the cost for each item to a running sum (price below). If the item is an ElectronicItem, invoke calculateCost method <u>and add the electronics surcharge</u> that was passed as a parameter to calculateTotal.</li>

</ul>

o <strong>Use the <em>instanceof</em> operator to determine whether an object is an instance of particular class</strong> (place this <em>if-else</em> inside the for loop). If the object is of type ElectronicsItem, the following code shows how the <em>instanceof</em> operator is used to add the small surcharge to an ElectronicsItem:




Add an else clause to calculate the cost without adding the surcharge:




<ul>

 <li>Be sure to <u>return total</u> after the loop.</li>

</ul>

<h1>Main Method</h1>

<ul>

 <li>In the main method, add code to print the total of all items and include an electronics surcharge of 2.0:</li>

 <li>Your output should appear as follows.</li>

</ul>

<table width="559">

 <tbody>

  <tr>

   <td width="559">ÏÏ«Ï —-jGRASP exec: java -ea InventoryListApp ÏÏ§Ï ÏÏ§ÏAll inventory: ÏÏ§ÏÏÏ§Ïlaptop: $1311.288ÏÏ§Ïmotor oil: $10.290000000000001ÏÏ§ÏAll Things Java – Author Not Listed: $12.3ÏÏ§ÏUseful Acronyms: $3.4ÏÏ§Ï ÏÏ§ÏTotal: 1339.278 ÏÏ§ÏÏÏ©Ï —-jGRASP: operation complete. </td>

  </tr>

 </tbody>

</table>

<strong> </strong> <strong>    </strong>

<h1>UML Class Diagram</h1>

<ul>

 <li>If you have not already done so, create a jGRASP project called InventoryListApp and add all of your classed for this activity.</li>

 <li>Generate theUML class diagram and arrange the class as shown below.<strong>    </strong></li>

</ul>

<h1>Viewer Canvas</h1>

<ul>

 <li>Create a canvas for your program as follows:

  <ul>

   <li>Run your program in the canvas . After the canvas opens, single step your program until you see myItems in the Debug tab.</li>

   <li>Drag myItems onto the canvas. Then select the inventory field in myItems and drag it out onto the canvas.</li>

   <li>Drag myItems onto the canvas again and change the viewer to the “toString” viewer. To do this, select the viewer window, click the menu button  on the top-right of the viewer frame, then select “Viewer” then “toString”.</li>

   <li>Save the canvas then end the program. Run your program in the canvas .  Now single step your program and watch the objects appear on the canvas.</li>

   <li>Run your program in the canvas . Click the play button and watch the canvas and stepping in the program as the objects appear on the canvas.  Notice that the debugger is stepping into each of your constructors and method as they are called.  You should be sure that your understand “how” your program is running to accomplish its task.  Note that you can pause the canvas and then hit play             to continue auto stepping-in.  You can also set one or more breakpoints and then resume to breakpoint.</li>

  </ul></li>

</ul>




<ul>

 <li>You should become comfortable using the canvas and debugger so that when needed, you will be able to use them to help find and correct errors in your projects.</li>

</ul>