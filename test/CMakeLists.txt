
file(GLOB sub_folders ./*)
foreach(folder ${sub_folders})
  if(IS_DIRECTORY ${folder})
    add_subdirectory(${folder})
  endif()
endforeach()
