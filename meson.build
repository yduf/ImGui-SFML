project('sfml', 'cpp',
  version : '0.1',
  default_options : ['warning_level=3'])

imgui_sfml = dependency('imgui-sfml')

exe = executable('sfml', 'main.cc',  dependencies : [ imgui_sfml],
  install : true)

test('basic', exe)
