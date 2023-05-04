Download Link: https://assignmentchef.com/product/solved-csc-110-fundamentals-of-programming-i-assignment-6-2-dimensional-arrays
<br>
<strong>Learning outcomes </strong>

When you have completed this assignment, you will understand:

<ul>

 <li>How to pass <em>parameters</em> and <em>return</em> values using static  How to pass arguments from the command-line to the String[] args array</li>

 <li>How to use <em>two-dimensional</em> (2D)</li>

 <li>How to orient yourself with and extend previously written code.  How to <em>indent </em>and<em> document</em> a Java program.</li>

</ul>

One well-known set of tasks for computers today is the manipulation of images.

Your work for this assignment is to add additional methods to the program

<strong>ImageManipulate.java</strong>. Each execution of the program will perform either one output transformation (ASCII-art version of image) or an image manipulation (i.e., reflect across x-axis; reflect across y-axis; tile an image; invert image, rotate image).

For this assignment, you will be using the command-line interface to pass in the names of the input and output files, as well as the image manipulation operation information. <strong>Solutions must not use a Scanner object</strong>, or require any other interaction from the user during execution.




To illustrate how the data in an image file is represented in a 2D array of integers, consider the very small image below that is 10 pixels wide by 10 pixels high below:

If we really zoom in on this image, we can see that the image is a matrix of pixels, each representing some shade of gray.  A 2D array of integers with values ranging from 0 to 255 to represent the above image could be constructed in our program. Given the image above named “example.png”, using the <strong>readGrayscaleImage</strong> method provided, we could create a 2D array with the same values shown above.

<strong>int[][] image = readGrayscaleImage(“example.png”); </strong>

The above statement would create an array with the same values as the following:

<strong>int[][] image = { </strong>

<strong>     {255, 255, 255, 255, 255, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>}, </strong>

<strong>     {255, 255, 255, 255, 255, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>}, </strong>

<strong>     {255, </strong>000<strong>, 253, 255, </strong>000<strong>, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>}, </strong>

<strong>     {255, </strong>000<strong>, 255, 255, </strong>000<strong>, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>}, </strong>

<strong>     {255, 255, 255, 255, 255, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>}, </strong>

<strong>     {255, 255, 255, 255, 255, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>}, </strong>

<strong>     {255, </strong>000<strong>, 255, 255, </strong>000<strong>, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>}, </strong>

<strong>     {255, </strong>000<strong>, 255, 255, </strong>000<strong>, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>}, </strong>

<strong>     {255, 255, </strong>000<strong>, </strong>000<strong>, 253, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>}, </strong>

<strong>     {255, 255, 255, 255, 255, 255, 255, </strong>000<strong>, </strong><strong>195</strong><strong>, </strong><strong>126</strong><strong>} }; </strong>

As you can see in the 2D array of integers above, all of the black pixels in the image have a value of 0, all of the white pixels in the image have a value of 255, and all the gray pixels have a value in between, depending on how light or dark they are.

<strong>Recommended steps to follow in order </strong>

<ol>

 <li>Similar to Assignments 4 &amp; 5, the <a href="https://connex.csc.uvic.ca/access/content/group/c695ec2f-7536-40a4-8ddc-eec4c5c20d41/Assignment%20Resources/Assignment6/ImageManipulate.html">specification document</a> outlines all of the required methods for this assignment. Appendix A illustrates some examples of how to call and test the methods in your ImageManipulate.java program.</li>

 <li>In this assignment the args array in the main method specifies the name of the input image file to read and output image file to create. It also specifies which method to run. Complete the main method first, by calling the readGrayscaleImage method, which creates a 2D array of integers from an image file. The array is what you will use in the manipulation methods.</li>

 <li>Now start working on the manipulation methods. Start with the invert This method returns a 2D array back to main with all values inverted. When this is complete, you can pass the resulting 2D array into the writeGrayscaleImage method, and see the inverted image!</li>

</ol>

<strong>Marking  </strong>

Your mark will be based on the following criteria:

<ul>

 <li>Your code <em>must compile and run</em>. Some examples of how to test your methods, along with expected output, are outlined in <strong>Appendix A.</strong></li>

 <li>Your code must conform to all the requirements mentioned in the <a href="https://connex.csc.uvic.ca/access/content/group/c695ec2f-7536-40a4-8ddc-eec4c5c20d41/Assignment%20Resources/Assignment6/ImageManipulate.html">specification document</a><a href="https://connex.csc.uvic.ca/access/content/group/c695ec2f-7536-40a4-8ddc-eec4c5c20d41/Assignment%20Resources/Assignment6/ImageManipulate.html">.</a></li>

 <li>Test each of the required methods to ensure each one functions correctly.</li>

 <li>Your code must follow the guidelines outlined in Style_Guidelines.pdf, found through the Lectures &amp; Stuff link in the Lab Resources folder on connex. You may notice that the specification document provides some very nice comments you are welcome to borrow.</li>

</ul>

<strong><u>Appendix A – Testing your code</u></strong>

<strong>Getting started setting up the </strong><em>main</em><strong> method: </strong>

All of the information needed by the program will be passed in through the args array when the program is executed, there will be <strong>no use of Scanners</strong>. Let’s assume the user compiled and executed the program the following way:

This will put the following contents into the args array in the main method:

<h1>args: {“example.jpg”,”invertTest.jpg”,”invert”} args.length: 3</h1>

This command tells your program to use the data in the <strong>example.jpg</strong> file, <strong>invert</strong> it, and create a new image file <strong>invertTest.jpg</strong> with the inverted values.

example.jpg                                                                  invertTest.jpg




The program will always be executed in the same  fashion:

<strong>java ImageManipulate &lt;inputFile&gt; &lt;outputFile&gt; &lt;operation&gt; </strong>

As shown above, the first argument is the input file’s name, the second argument is the output file’s name, and the remaining argument(s) are used to call the corresponding method in the program (the tile method actually requires 5 arguments).

In your main method, first ensure that args array has at least 3 elements in it. After this is done, you can begin to set-up your variables. Using the input file name (first argument), you can call the method readGrayscaleImage to create a 2D array of integers. Based on the operation name (third argument), one of the methods in your program will be called.  Each method manipulates the values in a 2D array of integers and returns a new array. This new array can be passed into the writeGrayscaleImage along with the output file name (second argument) to create a new image file. Open up the new file to see the results!




<em>invert</em> <strong>method:</strong>

Given there is an image file called “computer.jpg” in the same folder as the Java file, to create a new image file called “output.jpg” we would run our java program the following way:

<strong>java ImageManipulate computer.jpg output.jpg invert </strong>

Tips:

<ul>

 <li>The output image has the same dimensions (height and width) as the input image (so the 2D arrays of integers will be the same size)</li>

 <li>Inverting a number of a 10-point scale might be easier to think about (0 becomes 10, 1 becomes 9, 2 becomes 8, etc). For this case, we want to invert numbers on a 255-point scale. What is the pattern?</li>

</ul>

Given the file on left is “computer.jpg”, the following file will be created: <sub>f </sub>

<em>makeAscii</em> <strong>method: </strong>

Given there is an image file called “computer.jpg” in the same folder as the Java file, to create a new image file called “ascii.txt” using a <strong>PrintStream</strong>, we would run our java program the following way:

<strong>java ImageManipulate computer.jpg ascii.txt makeAscii </strong>

<strong><u>NOTE:</u></strong><u> For this operation the writeGrayscaleImage method is <strong>not</strong> called</u>

Tips:

<table>

 <tbody>

  <tr>

   <td width="58"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

1) Create a PrintStream to write each ASCII character into. Each character is based off of the integer value in the 2D array, using the following integer value to character mappings:

<table width="215">

 <tbody>

  <tr>

   <td width="96">Value</td>

   <td width="48"> </td>

   <td width="71">Character</td>

  </tr>

  <tr>

   <td width="96">0   to  20</td>

   <td width="48"> </td>

   <td width="71">M</td>

  </tr>

  <tr>

   <td width="96">21 to 40</td>

   <td width="48"> </td>

   <td width="71">L</td>

  </tr>

  <tr>

   <td width="96">41 to 60</td>

   <td width="48"> </td>

   <td width="71">I</td>

  </tr>

  <tr>

   <td width="96">61 to 80</td>

   <td width="48"> </td>

   <td width="71">o</td>

  </tr>

  <tr>

   <td width="96">81 to 100</td>

   <td width="48"> </td>

   <td width="71">|</td>

  </tr>

  <tr>

   <td width="96">101 to 120</td>

   <td width="48"> </td>

   <td width="71">=</td>

  </tr>

  <tr>

   <td width="96">121 to 140</td>

   <td width="48"> </td>

   <td width="71">*</td>

  </tr>

  <tr>

   <td width="96">141 to 160</td>

   <td width="48"> </td>

   <td width="71">:</td>

  </tr>

  <tr>

   <td width="96">161 to 180</td>

   <td width="48"> </td>

   <td width="71">–</td>

  </tr>

  <tr>

   <td width="96">181 to 200</td>

   <td width="48"> </td>

   <td width="71">,</td>

  </tr>

  <tr>

   <td width="96">201 to 220</td>

   <td width="48"> </td>

   <td width="71">.</td>

  </tr>

  <tr>

   <td width="96">221 to 255</td>

   <td width="48"> </td>

   <td width="71">  (space)</td>

  </tr>

 </tbody>

</table>

Given the file on left is “computer.jpg”, the following text file will be created: <sub>f </sub>

<em>tile</em> <strong>method: </strong>

Given there is an image file called “computer.jpg” in the same folder as the Java file, to create a new image file called “output.jpg” we would run our java program the following way:

<strong>java ImageManipulate computer.jpg output.jpg tile 2 3 </strong>

Tips:

<ul>

 <li>The output image’s height and width will be a multiple of the originals. If the parameters passed in are 5 and 7, the output image’s width will be 5x the original image’s width, and 7x the height of the original image.</li>

 <li>Each of the tiled images will be an exact replica of the original image. Given the file on left is “computer.jpg”, the following file will be created: <sub>f </sub></li>

</ul>




<em>verticalMirror</em> <strong>method: </strong>

Given there is an image file called “computer.jpg” in the same folder as the Java file, to create a new image file called “output.jpg” we would run our java program the following way:

<strong>java ImageManipulate computer.jpg output.jpg verticalMirror </strong>

Tips:

<ul>

 <li>This method reverses all of the values across each row in a 2D array. Think about how to reverse the values in an array.</li>

 <li>Each value does not move up or down a row, only its column number is changed.</li>

</ul>




Given the file on left is “computer.jpg”, the following file will be created:

<strong>             </strong>

<em>horizontalMirror</em> <strong>method: </strong>

Given there is an image file called “computer.jpg” in the same folder as the Java file, to create a new image file called “output.jpg” we would run our java program the following way:

<h1>java ImageManipulate computer.jpg output.jpg horizontalMirror</h1>

Tips:

<ul>

 <li>This method reverses all of the values down each column in a 2D array.</li>

 <li>Each value does not move left or right to a different column, only its row number is changed.</li>

</ul>

Given the file on left is “computer.jpg”, the following file will be created:

<strong>             </strong>

<em>rotate</em> <strong>method: </strong>

Given there is an image file called “computer.jpg” in the same folder as the Java file, to create a new image file called “output.jpg” we would run our java program the following way:

<strong>java ImageManipulate computer.jpg output.jpg rotate </strong>

Tips:

<ul>

 <li>If the image is not square, the output image’s height with be equal to original image’s width, and width equal to the original image’s height.</li>

 <li>Try creating a 2D array on paper and mapping out where each value in the array goes during a rotate. Try and find a pattern, and this should help with setting up your algorithm that you can use in your solution.</li>

</ul>

Given the file on left is “computer.jpg”, the following file will be created:

<span style="text-decoration: line-through;">R</span>


