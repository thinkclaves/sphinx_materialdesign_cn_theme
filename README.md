# Material Design HTML Theme for Sphinx

[![PyPI version](https://badge.fury.io/py/sphinx_materialdesign_theme.svg)](https://badge.fury.io/py/sphinx_materialdesign_theme)
[![CircleCI](https://circleci.com/gh/myyasuda/sphinx_materialdesign_theme.svg?style=svg)](https://circleci.com/gh/myyasuda/sphinx_materialdesign_theme)

[Demo Document](http://myyasuda.github.io/sphinx_materialdesign_theme)

## Requirements

- python
  - Sphinx

## Quick Start

Install the latest version of sphinx_materialdesign_theme with `pip`.

```shell
pip install sphinx_materialdesign_theme
```

Add the following line to `conf.py`.

```python
html_theme = 'sphinx_materialdesign_theme'
```

## Html theme options

The following is a description of the options that can be specified in `html_theme_options` in your project's `conf.py`.

```python
html_theme_options = {
    # Specify a list of menu in Header.
    # Tuples forms:
    #  ('Name', 'external url or path of pages in the document', boolean, 'icon name')
    #
    # Third argument:
    # True indicates an external link.
    # False indicates path of pages in the document.
    #
    # Fourth argument:
    # Specify the icon name.
    # For details see link.
    # https://material.io/icons/
    'header_links' : [
        ('Home', 'index', False, 'home'),
        ("ExternalLink", "http://example.com", True, 'launch'),
        ("NoIconLink", "http://example.com", True, ''),
        ("GitHub", "https://github.com/myyasuda/sphinx_materialdesign_theme", True, 'link')
    ],

    # Customize css colors.
    # For details see link.
    # https://getmdl.io/customize/index.html
    #
    # Values: amber, blue, brown, cyan deep_orange, deep_purple, green, grey, indigo, light_blue,
    #         light_green, lime, orange, pink, purple, red, teal, yellow(Default: indigo)
    'primary_color': 'indigo',
    # Values: Same as primary_color. (Default: pink)
    'accent_color': 'pink',

    # Customize layout.
    # For details see link.
    # https://getmdl.io/components/index.html#layout-section
    'fixed_drawer': True,
    'fixed_header': True,
    'header_waterfall': True,
    'header_scroll': False,

    # Render title in header.
    # Values: True, False (Default: False)
    'show_header_title': False,
    # Render title in drawer.
    # Values: True, False (Default: True)
    'show_drawer_title': True,
    # Render footer.
    # Values: True, False (Default: True)
    'show_footer': True
}
```
## Compile it to .whl

Make sure you have the latest versions of setuptools and wheel installed:
```
python3 -m pip install --user --upgrade setuptools wheel
```
Tip IF you have trouble installing these, see the Installing Packages tutorial.
Now run this command from the same directory where setup.py is located:
```
python3 setup.py sdist bdist_wheel
```
This command should output a lot of text and once completed should generate two files in the dist directory:
```
dist/
  example_pkg_your_username-0.0.1-py3-none-any.whl
  example_pkg_your_username-0.0.1.tar.gz
```
## Developer's Tips

### packaging

```
python setup.py sdist
```

### install

```
pip install dist/sphinx_materialdesign_theme-${version}.tar.gz
```

### Resister PyPI

```
python setup.py register sdist upload
```

### Build Example's Document

```
sphinx-build -b html ./example ./_build -c ./example
```

## License

|thirdparty              |version  |license         |URL                                                                |
|-----------------------|---------|----------------|-------------------------------------------------------------------|
| Material Design Lite  |1.3.0    | Apache 2.0     |https://github.com/google/material-design-lite/blob/mdl-1.x/LICENSE|
| Material design icons |3.0.1    | Apache 2.0     |https://github.com/google/material-design-icons/blob/master/LICENSE|
