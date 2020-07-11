# replace @datadir@ and translate
metadata = 'mate-abstract.xml'
i18n.merge_file(metadata,
  input: configure_file(
    input: metadata + '.in.in',
    output: metadata + '.in',
    configuration : conf
    ),
  output: metadata,
  po_dir: '../po',
  data_dirs: '..',
  install: true,
  install_dir: metadatadir
  )

backgrounds = [
  'Arc-Colors-Transparent-Wallpaper.png',
  'Flow.png',
  'Gulp.png',
  'Silk.png',
  'Spring.png',
  'Waves.png',
  'Elephants.jpg'
  ]
install_data(backgrounds, install_dir: join_paths(backgrounddir, 'abstract'))
