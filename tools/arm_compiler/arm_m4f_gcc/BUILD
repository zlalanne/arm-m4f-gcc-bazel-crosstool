package(default_visibility = ['//tools/arm_compiler:__pkg__'])

filegroup(
  name = 'gcc',
  srcs = [
    '@armGcc62017q2UpdateRepo//:gcc',
    'arm-none-eabi-gcc',
  ],
)

filegroup(
  name = 'ar',
  srcs = [
    '@armGcc62017q2UpdateRepo//:ar',
    'arm-none-eabi-ar',
  ],
)

filegroup(
  name = 'ld',
  srcs = [
    '@armGcc62017q2UpdateRepo//:ld',
    'arm-none-eabi-ld',
  ],
)

filegroup(
  name = 'nm',
  srcs = [
    '@armGcc62017q2UpdateRepo//:nm',
    'arm-none-eabi-nm',
  ],
)

filegroup(
  name = 'objcopy',
  srcs = [
    '@armGcc62017q2UpdateRepo//:objcopy',
    'arm-none-eabi-objcopy',
  ],
)

filegroup(
  name = 'objdump',
  srcs = [
    '@armGcc62017q2UpdateRepo//:objdump',
    'arm-none-eabi-objdump',
  ],
)

filegroup(
  name = 'strip',
  srcs = [
    '@armGcc62017q2UpdateRepo//:strip',
    'arm-none-eabi-strip',
  ],
)

filegroup(
  name = 'as',
  srcs = [
    '@armGcc62017q2UpdateRepo//:as',
    'arm-none-eabi-as',
  ],
)

filegroup(
  name = 'tool-wrappers',
  srcs = [
    ':gcc',
    ':ar',
    ':ld',
    ':nm',
    ':objcopy',
    ':objdump',
    ':strip',
    ':as',
  ],
)
