project('olcPixelGameEngine', 'cpp',
    default_options: ['cpp_std=c++17',
                      'default_library=static',
                      'buildtype=debugoptimized'])

pge_inc =include_directories('.')

pge_dep = declare_dependency(include_directories: pge_inc)

executable('sampleprog', 'olcExampleProgram.cpp')
