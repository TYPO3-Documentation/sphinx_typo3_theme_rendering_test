-------------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\Format\\CdataViewHelper
-------------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers\\Format

.. php:class:: CdataViewHelper

    Outputs an argument/value without any escaping and wraps it with CDATA tags.

    PAY SPECIAL ATTENTION TO SECURITY HERE (especially Cross Site Scripting),
    as the output is NOT SANITIZED!

    Examples
    ========

    Child nodes
    -----------

    ::

        <f:format.cdata>{string}</f:format.cdata>

    Output::

        <![CDATA[(Content of {string} without any conversion/escaping)]]>

    Value attribute
    ---------------

    ::

        <f:format.cdata value="{string}" />

    Output::

        <![CDATA[(Content of {string} without any conversion/escaping)]]>

    Inline notation
    ---------------

    ::

        {string -> f:format.cdata()}

    Output::

        <![CDATA[(Content of {string} without any conversion/escaping)]]>

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
