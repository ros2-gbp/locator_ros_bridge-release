[![License](https://img.shields.io/badge/License-Apache%202-blue.svg)](LICENSE)
[![Build status](http://build.ros.org/job/Ndev__locator_ros_bridge__ubuntu_focal_amd64/badge/icon?subject=Build%20farm%3A%20Noetic)](http://build.ros.org/job/Ndev__locator_ros_bridge__ubuntu_focal_amd64/)
[![Build status](http://build.ros2.org/job/Hdev__locator_ros_bridge__ubuntu_jammy_amd64/badge/icon?subject=Build%20farm%3A%20Humble)](https://build.ros2.org/job/Hdev__locator_ros_bridge__ubuntu_jammy_amd64/)
[![Build action: Noetic](https://github.com/boschglobal/locator_ros_bridge/actions/workflows/build_noetic.yml/badge.svg?branch=noetic)](https://github.com/boschglobal/locator_ros_bridge/actions/workflows/build_noetic.yml)
[![Build action: Humble](https://github.com/boschglobal/locator_ros_bridge/actions/workflows/build_humble.yml/badge.svg?branch=humble)](https://github.com/boschglobal/locator_ros_bridge/actions/workflows/build_humble.yml)
[![Build action (utils): Humble](https://github.com/boschglobal/locator_ros_bridge/actions/workflows/build_utils_humble.yml/badge.svg?branch=humble)](https://github.com/boschglobal/locator_ros_bridge/actions/workflows/build_utils_humble.yml)

---
**Level Up Your Mobile Robots. Rexroth ROKIT Locator – Your Easy-to-Use Laser Localization Software**

---

# locator_ros_bridge

This repository contains the [bosch_locator_bridge](bosch_locator_bridge) package, which provides a [ROS] interface to the [Rexroth ROKIT Locator].
It translates ROS messages to the ROKIT Locator API (as described in the ROKIT Locator API documentation) and vice versa.
It also allows to control the ROKIT Locator via ROS service calls.

There are versions for the following ROS 1 and ROS 2 distributions:
* ROS 1: Noetic (branch [noetic](../../tree/noetic), will likely also work on Melodic)
* ROS 2: Humble (this branch)

The repository also contains the [bosch_locator_bridge_utils](bosch_locator_bridge_utils) package, which provides an interface between the bosch_locator_bridge and [Nav2], the navigation stack of ROS 2.

The following video (click on image) gives more information about the ROKIT Locator.
[![Rexroth ROKIT Locator](https://dc-mkt-prod.cloud.bosch.tech/xrm/media/global/product_group_1/components_for_mobile_robotics/rokit/landingpage-stage-bild-keyvisual-locator-gruppe-a.jpg)](https://www.youtube.com/watch?v=g6SIUlXn9Bk)

## Installation

### Installing from Debian Package

You can install the `bosch_locator_bridge` package directly:

    sudo apt install ros-humble-bosch-locator-bridge

Note that the installed package may contain an older software version, which corresponds to the latest tag 2.1.x here: [tags].
Since the release of a package can take a while, the installed package may even be from an earlier tag.
To be sure, check the version of the installed package as follows:

    apt show ros-humble-bosch-locator-bridge

### Building from Source

#### Dependencies

- [ROS]
- [Poco] C++ library (Should be installed automatically with rosdep, otherwise try: ```sudo apt install libpoco-dev```)

#### Building

To build from source, make sure your colcon workspace is set up correctly. Then clone the latest version of this branch from the repository into your colcon workspace and compile the package using

    cd colcon_ws
    rosdep install --from-paths . --ignore-src
    colcon build --symlink-install

## How to Get Started

To get started, take a look at the [README.md](bosch_locator_bridge/README.md) of the bosch_locator_bridge package.
And for the bosch_locator_bridge_utils package, please have a look at [README.md](bosch_locator_bridge_utils/README.md).

## License

locator_ros_bridge is open-sourced under the Apache-2.0 license. See the [LICENSE](LICENSE) file for details.


[Nav2]: https://navigation.ros.org/
[ROS]: https://www.ros.org/
[Poco]: https://pocoproject.org/
[Rexroth ROKIT Locator]: https://www.boschrexroth.com/en/xc/products/product-groups/components-for-mobile-robotics/index
[tags]: https://github.com/boschglobal/locator_ros_bridge/tags
