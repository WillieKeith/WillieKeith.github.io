---
title: "Create a ROS Workspace (Robotics)"
date: 2024-05-19T13:04:43-04:00
author: "Weifan Zhou"
slug:
draft: false
toc: false
---
<div class = "reminder">Reminder: you need to set up ROS and linux before all the steps.</div>

1. In linux terminal, at your home directory, create a folder as your workspace directory using <code>mkdir [your folder name]</code>, for instance, <code>mkdir test_ws</code>.
2. Use <code>cd [your new folder name]</code>, for instance, <code>cd test_ws</code>, to navigaite into your directory. Then run <code>mkdir src</code> to create your source folder. (Tip: You can use <code>ls</code> to check what's inside your folder or directory.)
3. Use <code>cd src</code> to navigate into your new blank source folder. Then initialize catkin workspace by running <code>catkin_init_workspace</code>.
4. Go back to your folder by <code>cd ..</code>, press enter, then run <code>catkin_make</code>, which will create all shenanigans (I mean a bunch of files) for you.
5. <del>Now you need to source your file by <code>source devel/setup.bash</code>. Each time you run the program, you have to source your directory when you start your terminal by running <code>source [your directory name]/devel/setup.bash</code> after you open your linux terminal.</del> To avoid annoying steps, you can use <code>cd</code> to go back to your home directory, then open gedit (a text editor) by running <code>sudo gedit .bashrc</code> (remember to use <code>sudo install gedit</code> if you don't have one), enter your password, and then scroll down to the bottom of a bunch of test after a bunch of if statements. Add two lines of code: 
- <code>source /opt/ros/noetic/setup.bash</code> - <code>source ~/[your folder name]/devel/setup.bash</code>.
6. When ever you need to change the source (when you are working on different projects), for instance, from <code>test_ws</code> to <code>catkin_ws</code>, change the line, quote (using <code>#</code>) and create a new line, for instance:
    - <code>#source ~/catkin_ws/devel/setup.bash</code>
    - <code>source ~/test_ws/devel/setup.bash</code>
7. Congrats, you have created a new workspace!
---
#### ROS??? Tell me more about it.
To design and run a robot, one easy way is to use <a href="https://www.ros.org/">ROS</a>.

1. Why we use ROS?
- A lazy way to compile :P Otherwise you may need pointers and need to handle a bunch of annoying bugs.
2. System requirement?
- Linux. I use ubuntu 20.04.6. And if you are using windows 10 or 11, you can conside windows subsystem, which is the easiest way. Unfortunately, I forgot how to setup :( Check <a href="https://learn.microsoft.com/en-us/windows/wsl/install"> this document.</a> 
- The downside is, the subsystem doesn't have a graphic desktop prepared for you. Warning: if you are using ROS1, currently (May 2024) ROS1 cannot run on ubuntu 22. There're a bunch of tutorials on youtube regarding ros.
3. Recommended tutorials?
- I recommend this series. It includes ROS setup process. Click the link to see all the videos.
<iframe width="560" height="315" src="https://www.youtube.com/embed/Qk4vLFhvfbI?si=fxS7RV6uTU2ahvCs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
