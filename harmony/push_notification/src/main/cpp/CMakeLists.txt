# Copyright (c) Meta Platforms, Inc. and affiliates.
#
# This source code is licensed under the MIT license found in the
# LICENSE file in the root directory of this source tree.

cmake_minimum_required(VERSION 3.13)
set(CMAKE_VERBOSE_MAKEFILE on)

file(GLOB rnoh_push_notification_SRCS CONFIGURE_DEPENDS *.cpp)

add_library(
  rnoh_push_notification
  SHARED
  ${rnoh_push_notification_SRCS}
)

target_include_directories(rnoh_push_notification PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(rnoh_push_notification PUBLIC rnoh)
