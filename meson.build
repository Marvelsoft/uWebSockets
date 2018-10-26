project('uWebSocket', 'cpp',version: '0.14.8', default_options: ['cpp_std=c++14'])

comp_flags = ['-DUWS_THREADSAFE']


include = include_directories('include/uWS')
uWS_include = include_directories('include')
openssl_dep = dependency('openssl')
thread_dep = dependency('threads')
zlib_dep = dependency('zlib')

subdir('src')

uWS_deps =[ 
  declare_dependency(
    sources: uWS_src, 
    include_directories: include
    ), 
    openssl_dep,
    thread_dep,
    zlib_dep
] 

uWS_lib = shared_library('uWS',dependencies: uWS_deps,cpp_args: comp_flags)

uWS_dep = [
  declare_dependency(
    include_directories: uWS_include, 
    link_with: uWS_lib
    ),
    openssl_dep,
    thread_dep,
    zlib_dep
  ]



