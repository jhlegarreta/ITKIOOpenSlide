cmake_minimum_required(VERSION 3.10.2)

project(IOOpenSlide_Examples CXX)

find_package(ITK REQUIRED
  COMPONENTS
    ITKCommon
    ITKIOImageBase
    ITKIOTIFF
    IOOpenSlide
    ITKIOJPEG
    ITKIOPNG
  )
include(${ITK_USE_FILE})

add_definitions(-D_USE_MATH_DEFINES=1)

add_executable(DumpSlideInformation DumpSlideInformation.cxx)
target_link_libraries(DumpSlideInformation ${ITK_LIBRARIES})
