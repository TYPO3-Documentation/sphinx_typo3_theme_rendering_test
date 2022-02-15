-----------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\Format\\RawViewHelper
-----------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers\\Format

.. php:class:: RawViewHelper

    Outputs an argument/value without any escaping. Is normally used to output
    an ObjectAccessor which should not be escaped, but output as-is.

    PAY SPECIAL ATTENTION TO SECURITY HERE (especially Cross Site Scripting),
    as the output is NOT SANITIZED!

    Examples
    ========

    Child nodes
    -----------

    ::

        <f:format.raw>{string}</f:format.raw>

    Output::

        (Content of ``{string}`` without any conversion/escaping)

    Value attribute
    ---------------

    ::

        <f:format.raw value="{string}" />

    Output::

        (Content of ``{string}`` without any conversion/escaping)

    Inline notation
    ---------------

    ::

        {string -> f:format.raw()}

    Output::

        (Content of ``{string}`` without any conversion/escaping)

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
        :returns: mixed

    .. php:method:: compile($argumentsName, $closureName, $initializationPhpCode, ViewHelperNode $node, TemplateCompiler $compiler)

        :type $argumentsName: string
        :param $argumentsName:
        :type $closureName: string
        :param $closureName:
        :type $initializationPhpCode: string
        :param $initializationPhpCode:
        :type $node: ViewHelperNode
        :param $node:
        :type $compiler: TemplateCompiler
        :param $compiler:
        :returns: mixed
