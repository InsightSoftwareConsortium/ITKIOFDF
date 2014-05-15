PROJECT(ImageReadWrite)

# Find the ITK and VTK libraries

FIND_PACKAGE(ITK)
IF(ITK_FOUND)
   INCLUDE(${ITK_USE_FILE})
ELSE(ITK_FOUND)
   MESSAGE(FATAL_ERROR "Cannot build without ITK.  Please set ITK_DIR.")
ENDIF(ITK_FOUND)

FIND_PACKAGE(VTK)
IF (VTK_FOUND)
   INCLUDE (${VTK_USE_FILE})
ELSE(VTK_FOUND)
   MESSAGE(FATAL_ERROR
       "Cannot build without ITK.  Please set VTK_DIR.")
ENDIF(VTK_FOUND)

#---------------------------------------------------------------------------
# Our own app

ADD_EXECUTABLE(ImageReadWrite ImageReadWrite.cxx itkFDFImageIO.cxx itkFDFCommonImageIO.cxx itkFDFImageIOFactory.cxx)

# Optionally use vtkPatented libs (for Contouring/Marching Cubes)

TARGET_LINK_LIBRARIES(ImageReadWrite
        ITKCommon ITKIO ITKBasicFilters 
        vtkCommon vtkImaging vtkGraphics vtkIO vtkFiltering 
        vtkHybrid vtkRendering)
