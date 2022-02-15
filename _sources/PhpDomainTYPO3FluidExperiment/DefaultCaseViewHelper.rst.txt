-----------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\DefaultCaseViewHelper
-----------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: DefaultCaseViewHelper

    A ViewHelper which specifies the "default" case when used within the ``f:switch`` ViewHelper.

    .. php:attr:: escapeOutput

        protected boolean

    .. php:method:: render()

        :returns: string the contents of this ViewHelper if no other "Case" ViewHelper of the surrounding switch ViewHelper matches

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
