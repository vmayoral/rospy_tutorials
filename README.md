rospy_tutorials
===============

ROS python API tutorials code (check the wiki at http://ros.org/wiki/rospy_tutorials?distro=groovy)

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



