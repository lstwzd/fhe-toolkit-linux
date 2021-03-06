# Copyright (C) 2020 IBM Corp.
# This program is Licensed under the Apache License, Version 2.0
# (the "License"); you may not use this file except in compliance
# with the License. You may obtain a copy of the License at
#   http://www.apache.org/licenses/LICENSE-2.0
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License. See accompanying LICENSE file.

cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

## Use -std=c++17 as default.
set(CMAKE_CXX_STANDARD 17)
## Disable C++ extensions
set(CMAKE_CXX_EXTENSIONS OFF)
## Require full C++ standard
set(CMAKE_CXX_STANDARD_REQUIRED ON)
## Rely on the Environment variable to dictate which version of helib to use
set(HELIB_VERSION ${HELIB_CMAKE_LISTS_VERSON})

project(BGV_country_db_lookup
       	LANGUAGES CXX)

find_package(helib ${HELIB_VERSION} REQUIRED)

add_executable(BGV_country_db_lookup BGV_country_db_lookup.cpp)

target_link_libraries(BGV_country_db_lookup helib)

