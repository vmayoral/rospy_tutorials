rospy_tutorials
===============

This repository contains the rospy_tutorials code and the instructions to cross-compile this code to an embedded system using Angstrom.

For information about the ROS python API tutorials code check the wiki at http://ros.org/wiki/rospy_tutorials?distro=groovy
This code has been taken from the ros_tutorials code (https://github.com/ros/ros_tutorials) commit [b5dc0600481163e611ee838103836e76200b0ef8](https://github.com/ros/ros_tutorials/commit/b5dc0600481163e611ee838103836e76200b0ef8).

CROSS COMPILATION
=================

Recipes are available at https://github.com/vmayoral/beagle-ros/tree/master/recipes.


USAGE
=====

Cross-compile the code by yourself following these instructions (this has been tested using the BeagleBone):

* Set up an Angstrom distribution in your embedded platform. Some basic instructions about how to do to accomplish this are given at the `README.md`
of https://github.com/vmayoral/beagle-ros.

* `git clone` the beagle-ros project (https://github.com/vmayoral/beagle-ros.git) in some place such as `/tmp`

* add `recipes/*` to the `meta-ros/recipes-ros/`: `cp -r /path/to/beagle-ros/recipes/* /path/to/meta-ros/recipes-ros/`. This step adds the recipe required to cross-compile this code inside of the meta-ros
 code structure.

* `bitbake rospy-tutorials` to create an ipkg of the ROS package.

* copy `/path/to/the/package/*.ipkg` to your embedded platform and install it using `opkg install *.ipkg`

LICENSE
=======

The MIT License (MIT)

Copyright (c) 2013 Víctor Mayoral Vilches.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


