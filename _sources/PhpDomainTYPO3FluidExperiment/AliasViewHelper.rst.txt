-----------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\AliasViewHelper
-----------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: AliasViewHelper

    Declares new variables which are aliases of other variables.
    Takes a "map"-Parameter which is an associative array which defines the shorthand mapping.

    The variables are only declared inside the ``<f:alias>...</f:alias>`` tag. After the closing tag, all declared variables are removed again.

    Using this ViewHelper can be a sign of weak architecture. If you end up using it extensively you might want to fine-tune your "view model" (the data you assign to the view).

    Examples
    ========

    Single alias
    ------------

    ::

        <f:alias map="{x: 'foo'}">{x}</f:alias>

    Output::

        foo

    Multiple mappings
    -----------------

    ::

        <f:alias map="{x: foo.bar.baz, y: foo.bar.baz.name}">
            {x.name} or {y}
        </f:alias>

    Output::

        [name] or [name]

    Depending on ``{foo.bar.baz}``.

    .. php:attr:: escapeOutput

        protected boolean

    .. php:method:: initializeArguments()

        :returns: void

    .. php:method:: renderStatic($arguments, Closure $renderChildrenClosure, RenderingContextInterface $renderingContext)

        :type $arguments: array
        :param $arguments:
        :type $renderChildrenClosure: Closure
        :param $renderChildrenClosure:
        :type $renderingContext: RenderingContextInterface
        :param $renderingContext:
        :returns: mixed
