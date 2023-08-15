piper_phonemize_lib = static_library(
    'phonemize',
    'phonemize.cpp',
    'phoneme_ids.cpp',
    'tashkeel.cpp',
    dependencies: [espeak, onnxruntime],
)
piper_phonemize_dep = declare_dependency(
    dependencies: [espeak, onnxruntime],
    link_with: piper_phonemize_lib,
)

test(
    'phonemize',
    executable(
        'phonemize-test',
        'test.cpp',
        dependencies: [piper_phonemize_dep],
    ),

    args: ['/usr/lib/x86_64-linux-gnu/espeak-ng-data'],
    workdir: meson.project_source_root(),
)
