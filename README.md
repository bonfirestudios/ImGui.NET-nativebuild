# how to build

After syncing this repo:
`$ git submodule update --init --recursive`

Then, to build release version:
`$ ./build-native.cmd`

To build debug version:
`$ ./build-native.cmd Debug`

# Bonfire Notes

Install [cmake](https://cmake.org/download/) and add it to your path.  Version 3.27.6 should work.  I also [had to do this](https://stackoverflow.com/questions/56145118/cmake-cannot-open-ucrtd-lib/72297058#72297058).

This was forked from a fork that I found in a github issue addressing how to build implot and other extensions for imgui.net.

[These guys](https://github.com/ZingBallyhoo/ImGui.NET-nativebuild) are also maintaining what seems to be a rather up to date version of all these as well, so it might be a reference if you run into trouble.  Link to their [imgui.net fork](https://github.com/ZingBallyhoo/ImGui.NET) as well for reference.