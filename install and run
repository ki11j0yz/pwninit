<h1>pwninit</h1>
<p>I downloaded pwninit out of necessity for the PicoCTF <q>Cache Me Outside</q> in order to get the program to run locally on my machine.</p>
<p>I had issues with downloading it, getting it to run, and obtaining the necessary utilities for it to work correctly.</p>
<h3>The issues I created for myself:</h3>
<ul>
  <li>I was trying to clone the repository from the github source rather than use the 'wget' command (which I'm more familiar with). I don't have very much knowledge of using git, yet.</li>
  <li>I wasn't changing the permissions of the 'heapedit' file or the pwninit file that I downloaded. It was important to chmod +x both.</li>
  <li>I didn't have the necessary patchelf utility installed.</li>
  <li>Even though I read, and knew that the pwninit source states to RUN THE TOOL IN THE SAME DIRECTROY AS YOUR FILES, I still managed to mess that up - I'm not entirely sure how I did this but I think the mistake I was making was that I didn't give the PicoCTF files their OWN directory and then just move the tool into that directory and then run it.</li>
</ul>
<h3>What I did right...Finally.</h3>
<ul>
  <li>A little humility here, because once I figured out what I was doing wrong, I was able to reproduce what I did 3 other times on 3 other machines - which of course made me realize that what I was doing wrong was so simple.
</ul>
<ol>
  <li>For the sake of the ctf, I made a directory specifically for 'Cache Me Outside"</li>
  <li>I changed into that directory and used the wget command with this resource: https://github.com/io12/pwninit/releases/download/3.3.0/pwninit</li>
  <li>
	  I then copied the link addresses of the files from the ctf and used the wget command again to obtain all 3: https://mercury.picoctf.net/static/482492895851479e0da770f2892e2677/heapedit
https://mercury.picoctf.net/static/482492895851479e0da770f2892e2677/Makefile
https://mercury.picoctf.net/static/482492895851479e0da770f2892e2677/libc.so.6
  </li>
  <li>I made a 'flag.txt' file. In past ctf's, I've needed one beacuse some executables end up looking for one and if one isn't there - ya get an error.</li>
  <li>Once I had the heapedit file and pwninit in the same directory, I used 'chmod +x' to allow both files to become executable.</li>
  <li>I downloaded patchelf: $ sudo apt-get install patchelf</li>
  <li>I then ran pwninit using the correct syntax: $ ./pwninit --libc libc.so.6 --bin heapedit</li>
  <li>I then downloaded elfutils, because my original output mentioned needing it because it failed to unstrip libc: & sudo apt-get install elfutils </li>
</ol>	

![need elfutils](https://user-images.githubusercontent.com/116903454/209568394-8c0fd5e7-01c4-441f-bc24-956cf57a5359.png)


<h3>Steps I took in terminal</h3>






![pwninit solve](https://user-images.githubusercontent.com/116903454/209568645-61d9a1e7-afbb-4ef1-971d-7d2812e87bef.png)
