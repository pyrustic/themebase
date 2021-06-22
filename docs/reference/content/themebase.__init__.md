
Back to [Reference Overview](https://github.com/pyrustic/themebase/blob/master/docs/reference/README.md)

# themebase.\_\_init\_\_



<br>


```python

class Error:
    """
    Common base class for all non-exit exceptions.
    """

    def __init__(self, *args, **kwargs):
        """
        Initialize self.  See help(type(self)) for accurate signature.
        """

```

<br>

```python

class Theme:
    """
    A theme is a collection of styles and... others theme.
    """

    def __init__(self):
        """
        Initialize self.  See help(type(self)) for accurate signature.
        """

    @property
    def styles(self):
        """
        Get a list of styles that this theme contains
        """

    @property
    def themes(self):
        """
        Get a list of theme that this theme contains
        """

    def add_style(self, style, scope=None):
        """
        Add a style to this theme.
        The style is an instance of 'pyrustic.default_style._Style'.
        You don't have to directly subclass the private class '_Style'.
        Instead, subclass one of the public classes in the module 'pyrustic.default_style'.
        The scope here is an optional string.
        When you don't set the scope, the style will be applied as it.
        Example. If you add a Button style in your theme, this style will be
        applied to all buttons widgets. But you can restrict this effect to a scope.
        This scope could be by example "*Canvas*Button.", meaning all buttons
        that are living on all Canvas, are candidates for the given style.
        """

    def add_theme(self, theme):
        """
        Add a theme to this... theme
        """

    def target(self, master):
        """
        Set this theme to master. Master here should be the root widget of your app.
        You need to set the theme to master before installing others widgets on the master.
        """

```

