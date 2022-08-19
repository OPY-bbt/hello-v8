编译运行 v8

# Env
macOS Monterey 12.5.1

Xcode 13.4.1


# Steps
- install [depot_tools](https://commondatastorage.googleapis.com/chrome-infra-docs/flat/depot_tools/docs/html/depot_tools_tutorial.html#_setting_up)
- RUN `gclient`
- mkdir ~/v8
- cd ~/v8
- fetch v8
- cd v8
- RUN `gclient sync` (Download all the build dependencies)
- RUN `./tools/dev/gm.py arm64.release`
- now you can RUN `./out/arm64.release/d8 hello-world.js`

## run v8 in Xcode
- RUN `gn gen out/gn --ide="xcode"`
- open out/gn/all.xcodeproj
- Product > Scheme > Select d8
- build and run

## run samples/hello-world.cc
- Product > Scheme > Select v8_hello_world
- build and run


# Link
https://v8.dev/docs/build

https://v8.dev/docs/source-code

https://stackoverflow.com/questions/17980759/xcode-select-active-developer-directory-error/17980786#17980786

https://blog.csdn.net/i_can_/article/details/124086670