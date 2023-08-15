project('onnxruntime', 'cpp', version: '1.14.1')

cpp = meson.get_compiler('cpp')

onnxruntime_dep = declare_dependency(
    dependencies: cpp.find_library(
        'onnxruntime',
        dirs: [meson.current_source_dir() / 'lib'],
    ),
    include_directories: 'include',
)
