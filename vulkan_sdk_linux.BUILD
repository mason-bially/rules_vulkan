package(default_visibility = ["//visibility:public"])

alias(
    name = "glslangValidator",
    actual = "x86_64/bin/glslangValidator",
)

alias(
    name = "glslc",
    actual = "x86_64/bin/glslc",
)

alias(
    name = "spirv-as",
    actual = "x86_64/bin/spirv-as",
)

alias(
    name = "spirv-cfg",
    actual = "x86_64/bin/spirv-cfg",
)

alias(
    name = "spriv-cross", 
    actual = "x86_64/bin/spriv-cross",
)

alias(
    name = "spriv-dis",
    actual = "x86_64/bin/spriv-dis",
)

alias(
    name = "spirv-opt",
    actual = "x86_64/bin/spirv-opt",
)

alias(
    name = "spirv-remap",
    actual = "x86_64/bin/spirv-remap",
)

alias(
    name = "spirv-val",
    actual = "x86_64/bin/spirv-val",
)

cc_import(
    name = "vulkan-1",
    visibility = ["//visibility:private"],
    shared_library = "x86_64/lib/libvulkan.so.1",
)

cc_library(
    name = "vulkan",
    strip_include_prefix = "x86_64/include",
    hdrs = [
        "x86_64/include/vulkan/vk_icd.h",
        "x86_64/include/vulkan/vk_layer.h",
        "x86_64/include/vulkan/vk_platform.h",
        "x86_64/include/vulkan/vk_sdk_platform.h",
        "x86_64/include/vulkan/vulkan.h",
        "x86_64/include/vulkan/vulkan.hpp",
        "x86_64/include/vulkan/vulkan_android.h",
        "x86_64/include/vulkan/vulkan_core.h",
        "x86_64/include/vulkan/vulkan_fuchsia.h",
        "x86_64/include/vulkan/vulkan_ggp.h",
        "x86_64/include/vulkan/vulkan_ios.h",
        "x86_64/include/vulkan/vulkan_macos.h",
        "x86_64/include/vulkan/vulkan_metal.h",
        "x86_64/include/vulkan/vulkan_vi.h",
        "x86_64/include/vulkan/vulkan_wayland.h",
        "x86_64/include/vulkan/vulkan_win32.h",
        "x86_64/include/vulkan/vulkan_xcb.h",
        "x86_64/include/vulkan/vulkan_xlib.h",
        "x86_64/include/vulkan/vulkan_xlib_xrandr.h",
    ],
    deps = [":vulkan-1"],
)

cc_import(
    name = "shaderc_combined",
    visibility = ["//visibility:private"],
    interface_library = "x86_64/lib/shaderc_combined.so.1",
)

cc_library(
    name = "shaderc",
    strip_include_prefix = "x86_64/Include",
    hdrs = [
        "x86_64/Include/shaderc/env.h",
        "x86_64/Include/shaderc/shaderc.h",
        "x86_64/Include/shaderc/shaderc.hpp",
        "x86_64/Include/shaderc/status.h",
        "x86_64/Include/shaderc/visibility.h",
    ],
    deps = [":shaderc_combined"],
)

cc_library(
    name = "glslang",
    strip_include_prefix = "source/glslang",
    includes = [ "source/glslang" ],
    deps = [
        "//source/glslang:glslang", 
        "//source/glslang:SPIRV",
    ]
)
