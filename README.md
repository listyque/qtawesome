# QtAwesome

[![license](https://img.shields.io/pypi/l/qtawesome.svg)](./LICENSE)
[![pypi version](https://img.shields.io/pypi/v/qtawesome.svg)](https://pypi.org/project/qtawesome/)
[![conda version](https://img.shields.io/conda/vn/conda-forge/qtawesome.svg)](https://www.anaconda.com/download/)
[![download count](https://img.shields.io/conda/d/conda-forge/qtawesome.svg)](https://www.anaconda.com/download/)
[![OpenCollective Backers](https://opencollective.com/spyder/backers/badge.svg?color=blue)](#backers)
[![Join the chat at https://gitter.im/spyder-ide/public](https://badges.gitter.im/spyder-ide/spyder.svg)](https://gitter.im/spyder-ide/public)<br>
[![PyPI status](https://img.shields.io/pypi/status/qtawesome.svg)](https://github.com/spyder-ide/qtawesome)
[![Appveyor build status](https://ci.appveyor.com/api/projects/status/un8vnw4628cl6qfu?svg=true)](https://ci.appveyor.com/project/spyder-ide/qtawesome)
[![CircleCI build status](https://circleci.com/gh/spyder-ide/qtawesome/tree/master.svg?style=shield)](https://circleci.com/gh/spyder-ide/qtawesome/tree/master)
[![Documentation Status](https://readthedocs.org/projects/qtawesome/badge/?version=latest)](http://qtawesome.readthedocs.org/en/latest/?badge=latest)

*Copyright © 2015–2018 Spyder Project Contributors*


## Description

QtAwesome enables iconic fonts such as Font Awesome and Elusive Icons
in PyQt and PySide applications.

It started as a Python port of the [QtAwesome](
https://github.com/Gamecreature/qtawesome)
C++ library by Rick Blommers.


## Installation

Using `pip`:

Make sure you have [pip installed](https://pip.readthedocs.org/en/stable/installing/) and run:

```
pip install qtawesome
```

Using `conda`:

```
conda install qtawesome
```


## Examples

```python
import qtawesome as qta
```

- Use Font Awesome, Elusive Icons or Material Design Icons.

```python
# Get FontAwesome 5.x icons by name in various styles:
fa5_icon = qta.icon('fa5.flag')
fa5_button = QtGui.QPushButton(fa5_icon, 'Font Awesome! (regular)')
fa5s_icon = qta.icon('fa5s.flag')
fa5s_button = QtGui.QPushButton(fa5s_icon, 'Font Awesome! (solid)')
fa5b_icon = qta.icon('fa5b.github')
fa5b_button = QtGui.QPushButton(fa5b_icon, 'Font Awesome! (brands)')

# or Elusive Icons:
asl_icon = qta.icon('ei.asl')
elusive_button = QtGui.QPushButton(asl_icon, 'Elusive Icons!')

# or Material Design Icons:
apn_icon = qta.icon('mdi.access-point-network')
mdi_button = QtGui.QPushButton(apn_icon, 'Material Design Icons!')

```

- Apply some styling

```python
# Styling icons
styling_icon = qta.icon('fa5s.music',
                        active='fa5s.balance-scale',
                        color='blue',
                        color_active='orange')
music_button = QtGui.QPushButton(styling_icon, 'Styling')
```

- Stack multiple icons

```python
# Stacking icons
camera_ban = qta.icon('fa5s.camera', 'fa5s.ban',
                      options=[{'scale_factor': 0.5,
                                'active': 'fa5s.balance-scale'},
                               {'color': 'red'}])
stack_button = QtGui.QPushButton(camera_ban, 'Stack')
stack_button.setIconSize(QtCore.QSize(32, 32))
```

- Animations

```python
# Spining icons
spin_button = QtGui.QPushButton(' Spinning icon')
spin_icon = qta.icon('fa5s.spinner', color='red',
                     animation=qta.Spin(spin_button))
spin_button.setIcon(spin_icon)
```

- Screenshot

![QtAwesome screenshot](qtawesome-screenshot.gif)


## Other features

- QtAwesome comes bundled with Font Awesome and Elusive Icons, but it can also
  be used with other iconic fonts. The `load_font` function allows to load
  other fonts dynamically.
- QtAwesome relies on the [QtPy](https://github.com/spyder-ide/qtpy.git)
  project as a compatibility layer on the top ot PyQt or PySide.


## License

MIT License. Copyright 2015 - The Spyder development team.
See the [LICENSE](LICENSE) file for details.

The Font Awesome and Elusive Icons fonts are licensed under the SIL Open Font License.


## Contributing

Everyone is welcome to contribute!


## Backers

Support us with a monthly donation and help us continue our activities.

[![Backers](https://opencollective.com/spyder/backers.svg)](https://opencollective.com/spyder#support)


## Sponsors

Become a sponsor to get your logo on our README on Github.

[![Sponsors](https://opencollective.com/spyder/sponsors.svg)](https://opencollective.com/spyder#support)
