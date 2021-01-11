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
    name = "shaderc_combined",
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
    deps = [":shaderc_combined"],
)

cc_library(
    name = "glslang",
    strip_include_prefix = "glslang",
    includes = [ "glslang" ],
    hdrs = [
        "glslang/OGLCompilersDLL/InitializeDll.h",
        "glslang/SPIRV/GLSL.ext.EXT.h",
        "glslang/SPIRV/GLSL.ext.KHR.h",
        "glslang/SPIRV/GLSL.std.450.h",
        "glslang/SPIRV/GlslangToSpv.h",
        "glslang/SPIRV/Logger.h",
        "glslang/SPIRV/SPVRemapper.h",
        "glslang/SPIRV/SpvBuilder.h",
        "glslang/SPIRV/SpvTools.h",
        "glslang/SPIRV/bitutils.h",
        "glslang/SPIRV/disassemble.h",
        "glslang/SPIRV/doc.h",
        "glslang/SPIRV/hex_float.h",
        "glslang/SPIRV/spvIR.h",
        "glslang/SPIRV/spirv.hpp",
        "glslang/glslang/Include/BaseTypes.h",
        "glslang/glslang/Include/Common.h",
        "glslang/glslang/Include/ConstantUnion.h",
        "glslang/glslang/Include/InfoSink.h",
        "glslang/glslang/Include/InitializeGlobals.h",
        "glslang/glslang/Include/PoolAlloc.h",
        "glslang/glslang/Include/ResourceLimits.h",
        "glslang/glslang/Include/ShHandle.h",
        "glslang/glslang/Include/Types.h",
        "glslang/glslang/Include/arrays.h",
        "glslang/glslang/Include/intermediate.h",
        "glslang/glslang/Include/revision.h",
        "glslang/glslang/MachineIndependent/Initialize.h",
        "glslang/glslang/MachineIndependent/LiveTraverser.h",
        "glslang/glslang/MachineIndependent/ParseHelper.h",
        "glslang/glslang/MachineIndependent/RemoveTree.h",
        "glslang/glslang/MachineIndependent/Scan.h",
        "glslang/glslang/MachineIndependent/ScanContext.h",
        "glslang/glslang/MachineIndependent/SymbolTable.h",
        "glslang/glslang/MachineIndependent/Versions.h",
        "glslang/glslang/MachineIndependent/attribute.h",
        "glslang/glslang/MachineIndependent/gl_types.h",
        "glslang/glslang/MachineIndependent/glslang_tab.cpp.h",
        "glslang/glslang/MachineIndependent/iomapper.h",
        "glslang/glslang/MachineIndependent/localintermediate.h",
        "glslang/glslang/MachineIndependent/parseVersions.h",
        "glslang/glslang/MachineIndependent/preprocessor/PpContext.h",
        "glslang/glslang/MachineIndependent/preprocessor/PpTokens.h",
        "glslang/glslang/MachineIndependent/propagateNoContraction.h",
        "glslang/glslang/MachineIndependent/reflection.h",
        "glslang/glslang/OSDependent/osinclude.h",
        "glslang/glslang/Public/ShaderLang.h",

        "glslang/StandAlone/DirStackFileIncluder.h",
        "glslang/StandAlone/ResourceLimits.h",
    ],
    srcs = [
        "glslang/OGLCompilersDLL/InitializeDll.cpp",
        "glslang/SPIRV/GlslangToSpv.cpp",
        "glslang/SPIRV/InReadableOrder.cpp",
        "glslang/SPIRV/Logger.cpp",
        "glslang/SPIRV/SPVRemapper.cpp",
        "glslang/SPIRV/SpvBuilder.cpp",
        "glslang/SPIRV/SpvPostProcess.cpp",
        "glslang/SPIRV/SpvTools.cpp",
        "glslang/SPIRV/disassemble.cpp",
        "glslang/SPIRV/doc.cpp",
        "glslang/glslang/GenericCodeGen/CodeGen.cpp",
        "glslang/glslang/GenericCodeGen/Link.cpp",
        "glslang/glslang/MachineIndependent/Constant.cpp",
        "glslang/glslang/MachineIndependent/InfoSink.cpp",
        "glslang/glslang/MachineIndependent/Initialize.cpp",
        "glslang/glslang/MachineIndependent/IntermTraverse.cpp",
        "glslang/glslang/MachineIndependent/Intermediate.cpp",
        "glslang/glslang/MachineIndependent/ParseContextBase.cpp",
        "glslang/glslang/MachineIndependent/ParseHelper.cpp",
        "glslang/glslang/MachineIndependent/PoolAlloc.cpp",
        "glslang/glslang/MachineIndependent/RemoveTree.cpp",
        "glslang/glslang/MachineIndependent/Scan.cpp",
        "glslang/glslang/MachineIndependent/ShaderLang.cpp",
        "glslang/glslang/MachineIndependent/SymbolTable.cpp",
        "glslang/glslang/MachineIndependent/Versions.cpp",
        "glslang/glslang/MachineIndependent/attribute.cpp",
        "glslang/glslang/MachineIndependent/glslang_tab.cpp",
        "glslang/glslang/MachineIndependent/intermOut.cpp",
        "glslang/glslang/MachineIndependent/iomapper.cpp",
        "glslang/glslang/MachineIndependent/limits.cpp",
        "glslang/glslang/MachineIndependent/linkValidate.cpp",
        "glslang/glslang/MachineIndependent/parseConst.cpp",
        "glslang/glslang/MachineIndependent/preprocessor/Pp.cpp",
        "glslang/glslang/MachineIndependent/preprocessor/PpAtom.cpp",
        "glslang/glslang/MachineIndependent/preprocessor/PpContext.cpp",
        "glslang/glslang/MachineIndependent/preprocessor/PpScanner.cpp",
        "glslang/glslang/MachineIndependent/preprocessor/PpTokens.cpp",
        "glslang/glslang/MachineIndependent/propagateNoContraction.cpp",
        "glslang/glslang/MachineIndependent/reflection.cpp",

        "glslang/StandAlone/ResourceLimits.cpp",

        "glslang/glslang/OSDependent/Windows/ossource.cpp",
    ],
    local_defines = [ "GLSLANG_OSINCLUDE_WIN32" ],
)

# GLSL.std.450.h
# spirv.h
# spirv.hpp
# spirv.hpp11
# spirv.json
# spirv.lua
# spirv.py
