<h1>Update a file through a Python algorithm</h1>

<h2>Description</h2>

<p><em>This scenario was completed during the Google Cybersecurity Certificate Program:</em></p>

You are a security professional working at a health care company. As part of your job, you're required to regularly update a file that identifies the employees who can access restricted content. The contents of the file are based on who is working with personal patient records. Employees are restricted access based on their IP address. There is an allow list for IP addresses permitted to sign into the restricted subnetwork. There's also a remove list that identifies which employees you must remove from this allow list.

Your task is to create an algorithm that uses Python code to check whether the allow list contains any IP addresses identified on the remove list. If so, you should remove those IP addresses from the file containing the allow list.
<br />


<h2>Documentation provided</h2>

- <b>Instructions for including Python code</b>

<h2>Project walk-through:</h2>

<p align="left">
1. Open the file that contains the allow list<br/>
<br/>
In this scenario we want to open the file called "allow_list.txt" which contains a list of IP addresses permitted to sign into the restricted subnetwork First we assign a string containing this file name to the <strong>import_file</strong> variable. Then, use a <strong>with</strong> statement to open it (using the “r” argument so we can read). Finally, we’ll use the variable <strong>file</strong> to store the file while we work with it inside the <strong>with</strong> statement.
<br />
<img src="https://imgur.com/wdsbZod.png" height="80%" width="80%"/>
<br />
<br />
2. Read the file contents<br/>
<br/>
In order to read the files contents, we use the <strong>.read()</strong> method to convert the contents of the allow list file into a string so that you can read them. This string is then stored in a variable called <strong>ip_addresses</strong>.
<img src="https://imgur.com/rxl24Yr.png" height="80%" width="80%"/>
<br />
<br />
3. Convert the string into a list<br/>
<br/>
We have our list of IP addresses but it is in a single string format. To remove individual IP addresses from the allow list, the IP addresses need to be in a list format. To do this, we can use the <strong>.split()</strong> method to convert the ip_addresses string into a list. <br/>
<img src="https://imgur.com/Zbre6rX.png" height="80%" width="80%"/>
<br />
<br />
4. Iterate through the remove list<br/>
<br/>
A second list called <strong>remove_list</strong> contains all of the IP addresses that should be removed from the <strong>ip_addresses</strong> list. We can set up the header of a <strong>for</strong> loop that will iterate through the <strong>remove_list</strong> and use <strong>element</strong> as the loop variable.
<img src="https://imgur.com/5klS4Yx.png" height="80%" width="80%"/>
<br />
<br />
5. Remove IP addresses that are on the remove list<br/>
<br/>
Now we can add code to the body of our iterative statement that will remove all the IP addresses from the allow list that are also on the remove list. To do this we first create a conditional that evaluates if the loop variable <strong>element</strong> is part of the <strong>ip_addresses list</strong>. Then, within that conditional, apply the <strong>.remove()</strong> method to the <strong>ip_addresses</strong> list and remove the IP addresses identified in the loop variable <strong>element</strong>. Applying the <strong>.remove()</strong> method in this way is possible because there are no duplicates in the <strong>ip_addresses</strong> list.
<img src="https://imgur.com/8aDCsLS.png" height="80%" width="80%"/>
<br />
<br />
6. Update the file with the revised list of IP addresses<br/>
<br/>
With the invalid IP addresses removed from the <strong>ip_address</strong> variable, we can complete the algorithm by updating the file with this revised list. To do this, we must first convert the <strong>ip_addresses</strong> list back into a string using the <strong>.join()</strong> method. We apply <strong>.join()</strong> to the string " " in order to separate the elements in the file by a space.<br/>

Then, we use another <strong>with</strong> statement and the <strong>.write()</strong> method to write over the file assigned to the <strong>import_file</strong> variable.
<img src="https://imgur.com/UGmRybR.png" height="80%" width="80%"/>
<br />
<br />
7. Finalize your document by adding a Project description and Summary<br/>
<br/>
<strong>Project description</strong>
<br/>
In this project, we are a security professional working at a health care company. As part of our job, we’re required to regularly update a file that identifies the employees who can access restricted content. The contents of the file are based on who is working with personal patient records. Employees are restricted access based on their IP address. There is an allow list for IP addresses permitted to sign into the restricted subnetwork. There's also a remove list that identifies which employees we must remove from this allow list.

Our task is to create an algorithm that uses Python code to check whether the allow list contains any IP addresses identified on the remove list. If so, we should remove those IP addresses from the file containing the allow list.

<strong>Summary</strong>
<br/>
Our task was to create an algorithm that uses Python code to check whether the allow list contains any IP addresses identified on the remove list. If so, we should remove those IP addresses from the file containing the allow list.

We accomplished this task by
<ol>
<li>Opening the file that contains the allow list</li>
<li>Reading the file contents</li>
<li>Converting the string into a list</li>
<li>Iterating through the remove list</li>
<li>Removing any IP addresses that are on the remove list</li>
<li>Updating the file with the revised list of IP addresses</li>
</ol>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
