---
title: "ROS1: Create & Initialize a Ros Python Node (Author: Chat GPT)"
date: 2024-05-19T23:45:32-04:00
author: "Weifan Zhou"
slug:
draft: false
toc: false
---
<div class = "reminder">This note was originally written by Chat GPT 4o. I deleted one step.</div>

To create and initialize a ROS (Robot Operating System) Python file, follow these steps. This example assumes you are using ROS 1 (e.g., Melodic, Noetic).

### Prerequisites
1. **ROS Installation**: Make sure ROS is installed on your system.
2. **Workspace Setup**: You should have a ROS workspace set up (e.g., `catkin_ws`).

### Steps to Create and Initialize a ROS Python Node

1. **Create a New Package** (if you don’t already have one):
   ```bash
   cd ~/catkin_ws/src
   catkin_create_pkg my_package rospy std_msgs
   cd ~/catkin_ws
   catkin_make
   source devel/setup.bash
   ```

2. **Create the Python Node**:
   ```bash
   cd ~/catkin_ws/src/my_package/src
   touch my_node.py
   chmod +x my_node.py
   ```

3. **Edit the Python Node File** (`my_node.py`):
   Open `my_node.py` in your preferred text editor and add the following code to initialize a basic ROS node:
   ```python
   #!/usr/bin/env python3

   import rospy
   from std_msgs.msg import String

   def callback(data):
       rospy.loginfo(rospy.get_caller_id() + " I heard %s", data.data)

   def listener():
       # Initialize the node
       rospy.init_node('my_node', anonymous=True)

       # Subscribe to a topic (e.g., 'chatter')
       rospy.Subscriber("chatter", String, callback)

       # Keep python from exiting until this node is stopped
       rospy.spin()

   if __name__ == '__main__':
       try:
           listener()
       except rospy.ROSInterruptException:
           pass
   ```

4. **Run the Node**:
   Make sure the ROS master is running:
   ```bash
   roscore
   ```

   Open a new terminal, source your workspace, and run the node:
   ```bash
   cd ~/catkin_ws
   source devel/setup.bash    #See note
   rosrun my_package my_node.py
   ```

   <div class = "note">You can also use gedit. See my last note.</div>

5. **Publishing to the Node (for testing)**:
   Open another terminal, source your workspace, and publish to the `chatter` topic to see your node in action:
   ```bash
   cd ~/catkin_ws
   source devel/setup.bash    # You can also use gedit.
   rostopic pub /chatter std_msgs/String "Hello, ROS!" --once
   ```

Your node should now log the message "I heard Hello, ROS!" to the console.

### Summary
1. Create and initialize a ROS package.
2. Write a Python script for your ROS node.
3. Build your ROS workspace.
4. Run your ROS node and test it by publishing messages to the relevant topic.

This is a basic example to get you started with ROS and Python. You can expand on this by adding more functionality to your node, subscribing to different topics, or creating more complex ROS systems.