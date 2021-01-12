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

GLSLANG_HDRS = [
    "source/glslang/OGLCompilersDLL/InitializeDll.h",
    "source/glslang/SPIRV/GLSL.ext.EXT.h",
    "source/glslang/SPIRV/GLSL.ext.KHR.h",
    "source/glslang/SPIRV/GLSL.ext.NV.h",
    "source/glslang/SPIRV/GLSL.std.450.h",
    "source/glslang/SPIRV/GlslangToSpv.h",
    "source/glslang/SPIRV/Logger.h",
    "source/glslang/SPIRV/SPVRemapper.h",
    "source/glslang/SPIRV/SpvBuilder.h",
    "source/glslang/SPIRV/SpvTools.h",
    "source/glslang/SPIRV/bitutils.h",
    "source/glslang/SPIRV/disassemble.h",
    "source/glslang/SPIRV/doc.h",
    "source/glslang/SPIRV/hex_float.h",
    "source/glslang/SPIRV/spvIR.h",
    "source/glslang/SPIRV/spirv.hpp",
    "source/glslang/glslang/Include/BaseTypes.h",
    "source/glslang/glslang/Include/Common.h",
    "source/glslang/glslang/Include/ConstantUnion.h",
    "source/glslang/glslang/Include/InfoSink.h",
    "source/glslang/glslang/Include/InitializeGlobals.h",
    "source/glslang/glslang/Include/PoolAlloc.h",
    "source/glslang/glslang/Include/ResourceLimits.h",
    "source/glslang/glslang/Include/ShHandle.h",
    "source/glslang/glslang/Include/Types.h",
    "source/glslang/glslang/Include/arrays.h",
    "source/glslang/glslang/Include/intermediate.h",
    "source/glslang/glslang/Include/revision.h",
    "source/glslang/glslang/MachineIndependent/Initialize.h",
    "source/glslang/glslang/MachineIndependent/LiveTraverser.h",
    "source/glslang/glslang/MachineIndependent/ParseHelper.h",
    "source/glslang/glslang/MachineIndependent/RemoveTree.h",
    "source/glslang/glslang/MachineIndependent/Scan.h",
    "source/glslang/glslang/MachineIndependent/ScanContext.h",
    "source/glslang/glslang/MachineIndependent/SymbolTable.h",
    "source/glslang/glslang/MachineIndependent/Versions.h",
    "source/glslang/glslang/MachineIndependent/attribute.h",
    "source/glslang/glslang/MachineIndependent/gl_types.h",
    "source/glslang/glslang/MachineIndependent/glslang_tab.cpp.h",
    "source/glslang/glslang/MachineIndependent/iomapper.h",
    "source/glslang/glslang/MachineIndependent/localintermediate.h",
    "source/glslang/glslang/MachineIndependent/parseVersions.h",
    "source/glslang/glslang/MachineIndependent/preprocessor/PpContext.h",
    "source/glslang/glslang/MachineIndependent/preprocessor/PpTokens.h",
    "source/glslang/glslang/MachineIndependent/propagateNoContraction.h",
    "source/glslang/glslang/MachineIndependent/reflection.h",
    "source/glslang/glslang/OSDependent/osinclude.h",
    "source/glslang/glslang/Public/ShaderLang.h",

    "source/glslang/StandAlone/DirStackFileIncluder.h",
    "source/glslang/StandAlone/ResourceLimits.h",
]

cc_library(
    name = "glslang",
    strip_include_prefix = "source/glslang",
    includes = [ "source/glslang" ],
    hdrs = GLSLANG_HDRS,
    srcs = GLSLANG_HDRS + [
        "source/glslang/OGLCompilersDLL/InitializeDll.cpp",
        "source/glslang/SPIRV/GlslangToSpv.cpp",
        "source/glslang/SPIRV/InReadableOrder.cpp",
        "source/glslang/SPIRV/Logger.cpp",
        "source/glslang/SPIRV/SPVRemapper.cpp",
        "source/glslang/SPIRV/SpvBuilder.cpp",
        "source/glslang/SPIRV/SpvPostProcess.cpp",
        "source/glslang/SPIRV/SpvTools.cpp",
        "source/glslang/SPIRV/disassemble.cpp",
        "source/glslang/SPIRV/doc.cpp",
        "source/glslang/glslang/GenericCodeGen/CodeGen.cpp",
        "source/glslang/glslang/GenericCodeGen/Link.cpp",
        "source/glslang/glslang/MachineIndependent/Constant.cpp",
        "source/glslang/glslang/MachineIndependent/InfoSink.cpp",
        "source/glslang/glslang/MachineIndependent/Initialize.cpp",
        "source/glslang/glslang/MachineIndependent/IntermTraverse.cpp",
        "source/glslang/glslang/MachineIndependent/Intermediate.cpp",
        "source/glslang/glslang/MachineIndependent/ParseContextBase.cpp",
        "source/glslang/glslang/MachineIndependent/ParseHelper.cpp",
        "source/glslang/glslang/MachineIndependent/PoolAlloc.cpp",
        "source/glslang/glslang/MachineIndependent/RemoveTree.cpp",
        "source/glslang/glslang/MachineIndependent/Scan.cpp",
        "source/glslang/glslang/MachineIndependent/ShaderLang.cpp",
        "source/glslang/glslang/MachineIndependent/SymbolTable.cpp",
        "source/glslang/glslang/MachineIndependent/Versions.cpp",
        "source/glslang/glslang/MachineIndependent/attribute.cpp",
        "source/glslang/glslang/MachineIndependent/glslang_tab.cpp",
        "source/glslang/glslang/MachineIndependent/intermOut.cpp",
        "source/glslang/glslang/MachineIndependent/iomapper.cpp",
        "source/glslang/glslang/MachineIndependent/limits.cpp",
        "source/glslang/glslang/MachineIndependent/linkValidate.cpp",
        "source/glslang/glslang/MachineIndependent/parseConst.cpp",
        "source/glslang/glslang/MachineIndependent/preprocessor/Pp.cpp",
        "source/glslang/glslang/MachineIndependent/preprocessor/PpAtom.cpp",
        "source/glslang/glslang/MachineIndependent/preprocessor/PpContext.cpp",
        "source/glslang/glslang/MachineIndependent/preprocessor/PpScanner.cpp",
        "source/glslang/glslang/MachineIndependent/preprocessor/PpTokens.cpp",
        "source/glslang/glslang/MachineIndependent/propagateNoContraction.cpp",
        "source/glslang/glslang/MachineIndependent/reflection.cpp",

        "source/glslang/StandAlone/ResourceLimits.cpp",
        
        "source/glslang/glslang/OSDependent/Unix/ossource.cpp",
    ],
    local_defines = [ "GLSLANG_OSINCLUDE_UNIX" ],
)
