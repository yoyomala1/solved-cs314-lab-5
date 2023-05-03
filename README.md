Download Link: https://assignmentchef.com/product/solved-cs314-lab-5
<br>
<span class="kksr-muted">Rate this product</span>

Write a simple image processing application in C/C++.

The input to the application should be a ​ppm​ image file. There are many free utilities to convert from ​jpeg​ images to ​ppm​ ones.Your application must read this file and store the pixel information in a matrix.Then, it must perform two transformations to the image, ​one after the other​. Choose some simple transformations such as “RGB to grayscale”, “edge detection”, “image blur”, etc. Let us call the two transformations ​T1​ and ​T2​.

Write the resultant pixel matrix to a new ​ppm​ file.Usage: ./a.out &lt;path-to-original-image&gt; &lt;path-to-transformed-image&gt;

Now suppose you have a processor with two cores. You want your application to finish faster. You can do this by having the file read and ​T1​ done on the first core, passing the transformed pixels to the other core, where ​T2​ is performed on them, and then written to the output image file. Do this in the following ways:

<ol>

 <li>T1​ and ​T2​ are performed by 2 different threads of the same process. They communicate through the process’ address space itself.

  <ol>

   <li>Synchronization using atomic operations</li>

   <li>Synchronization using semaphores</li>

  </ol></li>

 <li>T1​ and ​T2​ are performed by 2 different processes that communicate via shared memory.Synchronization using semaphores.</li>

 <li>T1​ and ​T2​ are performed by 2 different processes that communicate via pipes.</li>

</ol>

<ul>

 <li>●  Briefly describe the chosen image transformations in your report.</li>

 <li>●  Devise a method to prove in each case that the pixels were received as sent, in the sentorder. Describe the method in your report.</li>

 <li>●  Study the run-time and speed-up of each of the approaches and discuss.</li>

 <li>●  Discuss the relative ease/ difficulty of implementing/ debugging each approach.</li>