cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(SegmentHumanBody)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/mazurowski-lab/SlicerSegmentHumanBody")
set(EXTENSION_CATEGORY "Segmentation")
set(EXTENSION_CONTRIBUTORS "Zafer Yildiz (Duke University - Mazurowski Lab)")
set(EXTENSION_DESCRIPTION "SegmentHumanBody aims to asist its users in segmenting medical data on 3D Slicer by comprehensively integrating the SegmentAnyBone developed by Mazurowski Lab.")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/mazurowski-lab/SlicerSegmentHumanBody/SegmentHumanBody/Resources/Icons/SegmentHumanBody.png")
set(EXTENSION_SCREENSHOTURLS "https://raw.githubusercontent.com/mazurowski-lab/SlicerSegmentHumanBody/Screenshots/sws1.png")
set(EXTENSION_DEPENDS "PyTorch") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(SegmentHumanBody)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
