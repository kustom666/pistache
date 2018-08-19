cxx_library(
  name = 'pistache',
  srcs = glob([
    'src/**/*.cc',
  ]),
  headers = subdir_glob([ # private include files
    ('include', '**/*.h'), # they are only accesible inside the library
    ('include', '**/*.hpp'),
  ]),
  exported_headers = subdir_glob([ # public include files
    ('include', '**/*.h'), # those will be exported
    ('include', '**/*.hpp'), # and accessible via <header.h>
  ]),
  visibility = ['PUBLIC']
)