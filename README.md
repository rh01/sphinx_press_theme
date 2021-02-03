# romnn's sphinx press theme

[![Build Status](https://github.com/romnn/sphinx_press_theme/workflows/test/badge.svg)](https://github.com/romnn/sphinx_press_theme/actions)
[![PyPI License](https://img.shields.io/pypi/l/romnnn_sphinx_press_theme)](https://pypi.org/project/romnnn_sphinx_press_theme/)
[![PyPI Version](https://img.shields.io/pypi/v/romnnn_sphinx_press_theme)](https://pypi.org/project/romnnn_sphinx_press_theme/)
[![PyPI Python versions](https://img.shields.io/pypi/pyversions/romnnn_sphinx_press_theme)](https://pypi.org/project/romnnn_sphinx_press_theme/)

See a [live demo](https://romnn.github.io/sphinx_press_theme).

This is a fork of the original [sphinx_press_theme](https://schettino72.github.io/sphinx_press_site/) by [schettino72](),
which is a modern and responsive theme for python's [Sphinx](http://www.sphinx-doc.org) documentation generator.

The theme is based on [VuePress](https://vuepress.vuejs.org/) and uses 
[Vue.js](https://vuejs.org/)+ 
[Stylus](http://stylus-lang.com/) with
[webpack](https://webpack.js.org/).

## Usage

First install the theme:
```bash
pip install romnnn_sphinx_press_theme
```

To use the theme, set the theme name to ``press`` in your sphinx project's ``conf.py``:
```python
html_theme = "press"
```

For more information, see the [Sphinx theming docs](http://www.sphinx-doc.org/en/master/theming.html#using-a-theme).

## Development
1. Build the web assets:
    ```bash
    cd ui
    npm run build
    ```

    The generated `theme.css`, `theme.js` and `theme-vendors.js` 
    will be linked into the theme under `romnn_sphinx_press_theme/static`.

2. Install theme locally:
    ```bash
    pip install -e .
   ```

3. Review the theme by building the theme's documentation under `docs/`:
    ```bash
    make docs
    ```

    Generated html will be in `docs/build/html`.
