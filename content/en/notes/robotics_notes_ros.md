---
title: "Create a ROS Workspace (Robotics)"
date: 2024-05-19T13:04:43-04:00
lastmod: 2024-05-21T13:47:22-06:00
author: "Weifan Zhou"
slug:
draft: false
toc: false
---
<div class = "reminder">Reminder: you need to set up ROS and Linux before all the steps.</div>

#### ROS??? Tell me more about it.
To design and run a robot, one easy way is to use <a href="https://www.ros.org/">ROS</a>.

1. Why we use ROS?
- A lazy way to compile :P Otherwise you may need pointers and need to handle a bunch of annoying bugs.
2. System requirement?
- Linux. I use ubuntu 20.04.6. And if you are using windows 10 or 11, you can conside windows subsystem, which is the easiest way. Unfortunately, I forgot how to setup :( Check <a href="https://learn.microsoft.com/en-us/windows/wsl/install"> this document.</a> 
- The downside of the subsyetem is, the subsystem doesn't have a graphic desktop prepared for you. Warning: if you are using ROS1, currently (May 2024) ROS1 cannot run on ubuntu 22. There're a bunch of tutorials on youtube regarding ros. If you can, use virtual machine, double system, or buy a hard drive and install Linux on that.
3. Recommended tutorials?
- I recommend this series. It includes ROS setup process. Click the link to see all 11 videos.
<iframe width="560" height="315" src="https://www.youtube.com/embed/Qk4vLFhvfbI?si=fxS7RV6uTU2ahvCs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---

#### Create a new workspace when you start a new project
1. In linux terminal, at your home directory, create a folder as your workspace directory using <code>mkdir [your folder name]</code>, for instance:
<code class="hljs properties">mkdir test_ws</code>

2. Use <code>cd [your new folder name]</code>, for instance, <code>cd test_ws</code>, to navigaite into your directory. Then run <code>mkdir src</code> to create your source folder. (Tip: You can use <code>ls</code> to check what's inside your folder or directory.) Here is an example for step 2:
<code class="hljs properties">cd test_ws <br> mkdir src<br> ls</code>

3. Use <code>cd src</code> to navigate into your new blank source folder. Then initialize catkin workspace. This is the code for step 3:
<code class="hljs properties">cd src <br> catkin_init_workspace</code>

4. <strong>(Important) </strong>Go back to the home directory of your workspace folder by <code>cd ..</code>, press enter, then run <code>catkin_make</code>, which will create all shenanigans (I mean a bunch of files) for you. Code for step 4:
<code class="hljs properties">cd .. <br> catkin_make</code>

5. <strong>(Important) </strong>Now you need to source your file by:
 <code class="hljs properties">source devel/setup.bash</code>

- Each time you run the program, you have to <strong>source</strong> your directory by <strong>running the line above. </strong>This is needed after you open your linux terminal, whenever do run the program, and whenever to switch to another robot project, etc. (Well, if you're not sure, just run it. It's not harmful).</del> 
- <strong>BUT THERE IS A TRICK :) </strong>There is a way that you don't need to source that often. Just run:
<code class="hljs properties">cd ..<br> sudo gedit .bashrc</code>
(Note: if there is an error, use <code>sudo install gedit</code> if your linux don't have gedit).

- Enter your password, and then scroll down to the bottom of a bunch of test after a bunch of if statements. Add two lines of code: 
<code class="hljs properties">source /opt/ros/noetic/setup.bash<br>source ~/[your folder name, for instance, test_ws]/devel/setup.bash</code>

- Congrats, you edited the code file! But to keep safe, I recommend after using gedit, still run source code whenever you are not sure if you should run it or not.

<div class = "reminder"> When ever you need to change the source (when you are working on different projects), for instance, from <code>test_ws</code> to <code>catkin_ws</code>, change the line, quote (using <code>#</code>) and create a new line, for instance:
<code class="hljs properties"> source ~/catkin_ws/devel/setup.bash <br> #source ~/test_ws/devel/setup.bash</code></div>

7. You've finished creating directories and soursing files. Now we need packages. Depending on the language you use (can be Python or C++), you may need different packages. Use <code>cd [your directory]/src</code> to your source folder (for instance, test_ws/src), and then type <code>catkin_create_pkg [your package folder] [all the shenanigans you need]</code>. If you need C++, use roscpp; if you use Python, use rospy. Here's the example code for step 7:
<code class="hljs properties">cd test_ws/src <br> catkin_create_pkg this_is_a_package roscpp rospy std_msg</code>

8. Congrats, you have created a new workspace with packages!
