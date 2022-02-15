-----------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\CountViewHelper
-----------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: CountViewHelper

    This ViewHelper counts elements of the specified array or countable object.

    Examples
    ========

    Count array elements
    --------------------

    ::

        <f:count subject="{0:1, 1:2, 2:3, 3:4}" />

    Output::

        4

    inline notation
    ---------------

    ::

        {objects -> f:count()}

    Output::

        10 (depending on the number of items in ``{objects}``)

    .. php:attr:: escapeChildren

        protected boolean

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
        :returns: integer
