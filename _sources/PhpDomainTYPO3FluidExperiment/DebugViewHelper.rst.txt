-----------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\DebugViewHelper
-----------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: DebugViewHelper

    This ViewHelper is only meant to be used during development.

    Examples
    ========

    Inline notation and custom title
    --------------------------------

    ::

        {object -> f:debug(title: 'Custom title')}

    Output::

        all properties of {object} nicely highlighted (with custom title)

    Only output the type
    --------------------

    ::

        {object -> f:debug(typeOnly: true)}

    Output::

        the type or class name of {object}

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
        :returns: string

    .. php:method:: dumpVariable($variable, $html, $level, $levels)

        :type $variable: mixed
        :param $variable:
        :type $html: boolean
        :param $html:
        :type $level: integer
        :param $level:
        :type $levels: integer
        :param $levels:
        :returns: string

    .. php:method:: getValuesOfNonScalarVariable($variable)

        :type $variable: mixed
        :param $variable:
        :returns: array
