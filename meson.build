project('olcPixelGameEngine', 'cpp',
    default_options: ['cpp_std=c++17',
                      'default_library=static',
                      'buildtype=debugoptimized'])

pge_inc = include_directories('.')
external_deps = [dependency('threads')]
cpp = meson.get_compiler('cpp')
if host_machine.system() == 'windows'
elif host_machine.system() == 'darwin'
  external_deps += [dependency('libpng'),
                    dependency('appleframeworks', modules: ['OpenGL', 'GLUT']),
                    ]
else
  external_deps += [dependency('libpng'),
                    dependency('gl'),
                    dependency('x11'),
                    cpp.find_library('stdc++fs', required: false)
                    ]
endif

pge_dep = declare_dependency(include_directories: pge_inc,
    dependencies: external_deps)

executable('sampleprog', 'olcExampleProgram.cpp',
   dependencies: external_deps)
