# Box2D CMake

This repository contains CMake files for Box2D based on [v2.3.1](https://github.com/erincatto/Box2D/tree/v2.3.1).

For help with Box2D, please visit http://www.box2d.org.

## Requirements

- C++11 compiler
- Box2D source files (see below)

## Build

To build Box2D with CMake clone Box2D and Box2D-cmake.

```
git clone https://github.com/erincatto/Box2D
git clone https://github.com/fxha/Box2D-cmake

cd Box2D
cp -R ../Box2D-cmake/Box2D .

mkdir Build
cd Build
cmake ../Box2D
make
```

Install library:

```
make install
```

## CMake options

| Option             | Description                              | Default |
| ------------------ | ---------------------------------------- | ------- |
| BOX2D_INSTALL      | Install Box2D library, includes, and CMake scripts | off     |
| BOX2D_BUILD_SHARED | Build Box2D shared library               | on      |

## Installation

### As CMake target

```
add_subdirectory(%path_to_box2d_with_cmake%)

target_link_libraries(%custom_target% Box2D)
```

### As CMake package

First of all install Box2D or build it yourself and `make install`.

```
find_package(Box2D REQUIRED)
include_directories(${Box2D_SOURCE_DIR})
target_link_libraries(%custom_target% Box2D)
```

## License

[zlib license](LICENSE)
