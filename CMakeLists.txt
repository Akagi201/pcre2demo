cmake_minimum_required(VERSION 3.25)

project(pcre2demo)

set(SOURCE_FILES src/pcre2demo.c)

include_directories("/usr/local/include" ${PROJECT_SOURCE_DIR}/src)

link_directories("/usr/local/lib")

include(cmake/CPM.cmake)

CPMAddPackage(
  NAME pcre2
  GITHUB_REPOSITORY PCRE2Project/pcre2
  GIT_TAG pcre2-10.40
  OPTIONS
    "BUILD_STATIC_LIBS ON"
    "PCRE2_STATIC_PIC ON"
)

add_executable(pcre2demo ${SOURCE_FILES})
target_link_libraries(pcre2demo pcre2-8)
