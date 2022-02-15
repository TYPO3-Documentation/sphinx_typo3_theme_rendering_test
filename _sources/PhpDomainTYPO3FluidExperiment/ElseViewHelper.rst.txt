----------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\ElseViewHelper
----------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: ElseViewHelper

    Else-Branch of a condition. Only has an effect inside of ``f:if``.
    See the ``f:if`` ViewHelper for documentation.

    Examples
    ========

    Output content if condition is not met
    --------------------------------------

    ::

        <f:if condition="{someCondition}">
            <f:else>
                condition was not true
            </f:else>
        </f:if>

    Output::

        Everything inside the "else" tag is displayed if the condition evaluates to FALSE.
        Otherwise nothing is outputted in this example.

    .. php:attr:: escapeOutput

        protected boolean

    .. php:method:: initializeArguments()

        :returns: void

    .. php:method:: render()

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
        :returns: string|NULL
