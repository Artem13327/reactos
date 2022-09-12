
add_library(uniata MODULE atapi.c atapi.rc)
target_link_libraries(uniata libcntpr)
set_module_type(uniata kernelmodedriver)
add_importlibs(uniata scsiport)
add_cd_file(TARGET uniata DESTINATION reactos/system32/drivers NO_CAB FOR all)
