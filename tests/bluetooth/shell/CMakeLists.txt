include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(NONE)
set(QEMU_EXTRA_FLAGS -serial unix:/tmp/bt-server-bredr)

zephyr_library_include_directories($ENV{ZEPHYR_BASE}/samples/bluetooth)
FILE(GLOB app_sources src/*.c)
target_sources(app PRIVATE ${app_sources})
