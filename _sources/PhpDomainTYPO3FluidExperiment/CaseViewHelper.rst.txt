----------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\CaseViewHelper
----------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: CaseViewHelper

    Case ViewHelper that is only usable within the ``f:switch`` ViewHelper.

    .. php:attr:: escapeOutput

        protected boolean

    .. php:method:: initializeArguments()

        :returns: void

    .. php:method:: render()

        :returns: string the contents of this ViewHelper if $value equals the expression of the surrounding switch ViewHelper, otherwise an empty string

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
