# use the include command in the calling CMakeLists.txt file with this file as an argument.

# The sources in this directory that are needed for compilation.
target_sources(acm PUBLIC
    "${CMAKE_CURRENT_LIST_DIR}/acm.cpp"
    "${CMAKE_CURRENT_LIST_DIR}/tool.cpp"
    "${CMAKE_CURRENT_LIST_DIR}/utilities.cpp"
    )

# Include here all the relevant code for the above sources.
# Use this project's base source directory for these paths.
target_include_directories(acm PUBLIC
    "${acm_SOURCE_DIR}/include"
    "${acm_SOURCE_DIR}/include/catch"
    "${acm_SOURCE_DIR}/include/rapidjson"
    "${acm_SOURCE_DIR}/include/spdlog"
    "${acm_SOURCE_DIR}/j2735/include"
    "${acm_SOURCE_DIR}/asn1c_j2735"
    "${acm_SOURCE_DIR}/asn1c/skeletons"
    )
