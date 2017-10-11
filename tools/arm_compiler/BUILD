# This is the entry point for --crosstool_top.
#
# The cc_toolchain rule used is found by:
#
# 1. Finding the appropriate toolchain in the CROSSTOOL file based on the --cpu
#    and --compiler command line flags (if they exist, otherwise using the
#    "default_target_cpu" / "default_toolchain" fields in the CROSSTOOL file)
# 2. Concatenating the "target_cpu" and "compiler" fields of the toolchain in
#    use and using that as a key in the map in the "toolchains" attribute
cc_toolchain_suite(
  name = 'toolchain',
  toolchains = {
    'arm-none-eabi-m4f|gcc': ':cc-compiler-arm-none-eabi-m4f',
  },
)

filegroup(
  name = 'arm_m4f_all_files',
  srcs = [
    '//tools/arm_compiler/arm_m4f_gcc:tool-wrappers',
    '@armGcc62017q2UpdateRepo//:compiler_pieces',
  ],
)

filegroup(
  name = 'arm_m4f_linker_files',
  srcs = [
    '//tools/arm_compiler/arm_m4f_gcc:gcc',
    '//tools/arm_compiler/arm_m4f_gcc:ld',
    '//tools/arm_compiler/arm_m4f_gcc:ar',
    '@armGcc62017q2UpdateRepo//:compiler_pieces',
  ],
)

filegroup(
  name = 'arm_m4f_compiler_files',
  srcs = [
    '//tools/arm_compiler/arm_m4f_gcc:gcc',
    '//tools/arm_compiler/arm_m4f_gcc:ld',
    '//tools/arm_compiler/arm_m4f_gcc:as',
  ],
)

cc_toolchain(
  name = 'cc-compiler-arm-none-eabi-m4f',
  all_files = ':arm_m4f_all_files',
  compiler_files = ':arm_m4f_compiler_files',
  cpu = 'arm-none-eabi-m4f',
  dwp_files = ':empty',
  dynamic_runtime_libs = [':empty'],
  linker_files = ':arm_m4f_linker_files',
  objcopy_files = '//tools/arm_compiler/arm_m4f_gcc:objcopy',
  static_runtime_libs = [':empty'],
  strip_files = '//tools/arm_compiler/arm_m4f_gcc:strip',
  supports_param_files = 1,
)
