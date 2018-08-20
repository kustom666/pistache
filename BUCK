prebuilt_cxx_library(
  name = 'pthread',
  header_only = True,
  exported_linker_flags = [
    '-lpthread',
  ],
)

cxx_library(
  name = 'pistache',
  header_namespace = 'pistache',
  srcs = glob([
    'src/**/*.cc',
  ]),
  headers = subdir_glob([ # private include files
    ('include/pistache', '**/*.h'), # they are only accesible inside the library
    ('include/pistache', '**/*.hpp'),
  ]),
  exported_headers = subdir_glob([ # public include files
    ('include/pistache', '**/*.h'), # those will be exported
    ('include/pistache', '**/*.hpp'), # and accessible via <header.h>
  ]),
  deps = [
    ':pthread',
  ],
  visibility = ['PUBLIC']
)