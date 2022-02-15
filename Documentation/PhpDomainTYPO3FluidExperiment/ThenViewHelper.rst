----------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\ThenViewHelper
----------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: ThenViewHelper

    ``f:then`` only has an effect inside of ``f:if``. See the ``f:if`` ViewHelper for documentation.

    .. php:attr:: escapeOutput

        protected boolean

    .. php:method:: render()

        Just render everything.

        :returns: string the rendered string

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
        :returns: string
