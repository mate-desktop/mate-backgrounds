# replace @datadir@ and translate
metadata = 'mate-desktop.xml'
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
  'Float-into-MATE.png',
  'GreenTraditional.jpg',
  'MATE-Stripes-Dark.png',
  'MATE-Stripes-Light.png',
  'Stripes.png',
  'Ubuntu-Mate-Cold-no-logo.png',
  'Ubuntu-Mate-Dark-no-logo.png',
  'Ubuntu-Mate-Radioactive-no-logo.png',
  'Ubuntu-Mate-Warm-no-logo.png',
]
install_data(backgrounds, install_dir: join_paths(backgrounddir, 'desktop'))
