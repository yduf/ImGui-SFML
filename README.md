# ImGui + SFML Tutorial

Drom [ImGui + SFML Tutorial - Install & Basics](https://www.youtube.com/watch?v=2YS5WJTeKpI)
- [imgui-sfml](https://github.com/SFML/imgui-sfml?tab=readme-ov-file#imgui-sfml) - a Library which allows you to use Dear ImGui with SFML

Tailored to compile on linux with meson build system

## Setup

This should compile with [meson](https://mesonbuild.com/index.html)

Imgui & [sfml](https://www.sfml-dev.org/tutorials/2.6/start-linux.php) are require to already be installed by imgui-sfml
```bash
$ sudo apt-get install libimgui-dev
$ sudo apt-get install libsfml-dev
```

To compile
```bash
$ meson build . # will install  imgui-sfml as a subproject -> see Note to fix error
$ cd build
$ meson compile
```

**Note**: There is a bug in `subprojects/imgui-sfml-2.6/meson.build`
and should update the dependency on sfml to `sfml_dep = dependency('sfml-all')` otherwise pkg-config won't work

