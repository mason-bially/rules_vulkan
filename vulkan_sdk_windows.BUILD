package(default_visibility = ["//visibility:public"])

alias(
    name = "glslangValidator",
    actual = "Bin/glslangValidator.exe",
)

alias(
    name = "glslc",
    actual = "Bin/glslc.exe",
)

alias(
    name = "spirv-as",
    actual = "Bin/spirv-as.exe",
)

alias(
    name = "spirv-cfg",
    actual = "Bin/spirv-cfg.exe",
)

alias(
    name = "spriv-cross",
    actual = "Bin/spriv-cross.exe",
)

alias(
    name = "spriv-dis",
    actual = "Bin/spriv-dis.exe",
)

alias(
    name = "spirv-opt",
    actual = "Bin/spirv-opt.exe",
)

alias(
    name = "spirv-remap",
    actual = "Bin/spirv-remap.exe",
)

alias(
    name = "spirv-val",
    actual = "Bin/spirv-val.exe",
)

cc_import(
    name = "vulkan-1",
    visibility = ["//visibility:private"],
    interface_library = "Lib/vulkan-1.lib",
    system_provided = True,
)

cc_library(
    name = "vulkan",
    strip_include_prefix = "Include",
    hdrs = [
        "Include/vulkan/vk_icd.h",
        "Include/vulkan/vk_layer.h",
        "Include/vulkan/vk_platform.h",
        "Include/vulkan/vk_sdk_platform.h",
        "Include/vulkan/vulkan.h",
        "Include/vulkan/vulkan.hpp",
        "Include/vulkan/vulkan_android.h",
        "Include/vulkan/vulkan_core.h",
        "Include/vulkan/vulkan_fuchsia.h",
        "Include/vulkan/vulkan_ggp.h",
        "Include/vulkan/vulkan_ios.h",
        "Include/vulkan/vulkan_macos.h",
        "Include/vulkan/vulkan_metal.h",
        "Include/vulkan/vulkan_vi.h",
        "Include/vulkan/vulkan_wayland.h",
        "Include/vulkan/vulkan_win32.h",
        "Include/vulkan/vulkan_xcb.h",
        "Include/vulkan/vulkan_xlib.h",
        "Include/vulkan/vulkan_xlib_xrandr.h",
    ],
    deps = [":vulkan-1"],
)

cc_import(
    name = "shaderc_combined_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/shaderc_combined.lib",
)

cc_library(
    name = "shaderc",
    strip_include_prefix = "Include",
    hdrs = [
        "Include/shaderc/env.h",
        "Include/shaderc/shaderc.h",
        "Include/shaderc/shaderc.hpp",
        "Include/shaderc/status.h",
        "Include/shaderc/visibility.h",
    ],
    deps = [":shaderc_combined_lib"],
)


cc_import(
    name = "glslang_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/glslang.lib",
)
cc_import(
    name = "GenericCodeGen_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/GenericCodeGen.lib",
)
cc_import(
    name = "OGLCompiler_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/OGLCompiler.lib",
)
cc_import(
    name = "OSDependent_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/OSDependent.lib",
)
cc_import(
    name = "MachineIndependent_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/MachineIndependent.lib",
)
cc_import(
    name = "HLSL_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/HLSL.lib",
)

cc_import(
    name = "spirv-cross-glsl_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/spirv-cross-glsl.lib",
)

cc_import(
    name = "SPIRV_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/SPIRV.lib",
)
cc_import(
    name = "SPIRV-Tools_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/SPIRV-Tools.lib",
)
cc_import(
    name = "SPIRV-Tools-link_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/SPIRV-Tools-link.lib",
)
cc_import(
    name = "SPIRV-Tools-opt_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/SPIRV-Tools-opt.lib",
)
cc_import(
    name = "SPIRV-Tools-reduce_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/SPIRV-Tools-reduce.lib",
)
cc_import(
    name = "SPIRV-Tools-shared_lib",
    visibility = ["//visibility:private"],
    static_library = "Lib/SPIRV-Tools-shared.lib",
)

cc_library(
    name = "glslang_SPIRV",
    strip_include_prefix = "Include/glslang",
    hdrs = glob(["Include/glslang/SPIRV/*.h*"]),
    deps = [
    ],
)

cc_library(
    name = "glslang",
    strip_include_prefix = "Include",
    hdrs = glob(["Include/glslang/**/*.h*"]),
    deps = [
        ":glslang_SPIRV",
        #":glslang_lib",
        #":HLSL_lib",
        ":GenericCodeGen_lib",
        ":OGLCompiler_lib",
        ":OSDependent_lib",
        ":MachineIndependent_lib",
        #":spirv-cross-glsl_lib",
        ":SPIRV_lib",
        ":SPIRV-Tools_lib",
        #":SPIRV-Tools-link_lib",
        ":SPIRV-Tools-opt_lib",
        #":SPIRV-Tools-reduce_lib",
        #":SPIRV-Tools-shared_lib",
    ],
)


# GLSL.std.450.h
# spirv.h
# spirv.hpp
# spirv.hpp11
# spirv.json
# spirv.lua
# spirv.py
