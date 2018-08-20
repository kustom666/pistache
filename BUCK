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
    ('include', '**/*.h'), # those will be exported
    ('include', '**/*.hpp'), # and accessible via <header.h>
  ]),
  visibility = ['PUBLIC']
)