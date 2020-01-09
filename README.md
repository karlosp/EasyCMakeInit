# EasyCMakeInit
GUI for easy and quick CMakeLists.txt generation

Start literature!
https://github.com/peter-can-talk/cppnow-2017/blob/master/code/cppgrep/cppgrep.cpp
https://www.youtube.com/watch?v=E6i8jmiy8MY

http://clang.llvm.org/docs/LibASTMatchersTutorial.html

project(GuiModelTestC CXX)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
  # As moc files are generated in the binary dir, tell CMake
  # to always look for includes there:
set(CMAKE_INCLUDE_CURRENT_DIR ON)

add_executable(GuiModelTestC mainwindow.h mainwindow.cpp main.cpp mainwindow.ui  )

find_package(Qt5 REQUIRED Widgets)
#target_link_libraries(GuiModelTestC
#  Core
#  Gui
#  Widgets)

qt5_use_modules(GuiModelTestC Widgets)
