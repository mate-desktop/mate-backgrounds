# replace @datadir@ and translate
metadata = 'mate-nature.xml'
i18n.merge_file(
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
  'Aqua.jpg',
  'Blinds.jpg',
  'Dune.jpg',
  'FreshFlower.jpg',
  'Garden.jpg',
  'GreenMeadow.jpg',
  'LadyBird.jpg',
  'RainDrops.jpg',
  'Storm.jpg',
  'TwoWings.jpg',
  'Wood.jpg',
  'YellowFlower.jpg',
]
install_data(backgrounds, install_dir: join_paths(backgrounddir, 'nature'))
