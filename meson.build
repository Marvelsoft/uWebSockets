project('uWebSocket', 'cpp',version: '0.14.8', default_options: ['cpp_std=c++14'])

comp_flags = ['-DUWS_THREADSAFE']


uWS_include = include_directories('include')

openssl_dep = dependency('openssl')
thread_dep = dependency('threads')
zlib_dep = dependency('zlib')

subdir('src')

uWS_dep =[ 
  declare_dependency(
    sources: uWS_src, 
    include_directories: uWS_include
    ), 
    openssl_dep,
    thread_dep,
    zlib_dep
] 

uWS_lib = shared_library('uWS',dependencies: uWS_dep,cpp_args: comp_flags)



