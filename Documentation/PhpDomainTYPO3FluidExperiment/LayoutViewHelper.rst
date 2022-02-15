------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\LayoutViewHelper
------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: LayoutViewHelper

    With this tag, you can select a layout to be used for the current template.

    Examples
    ========

    ::

        <f:layout name="main" />

    Output::

        (no output)

    .. php:method:: initializeArguments()

        Initialize arguments

        :returns: void

    .. php:method:: postParseEvent(ViewHelperNode $node, $arguments, VariableProviderInterface $variableContainer)

        On the post parse event, add the "layoutName" variable to the variable
        container so it can be used by the TemplateView.

        :type $node: ViewHelperNode
        :param $node:
        :type $arguments: array
        :param $arguments:
        :type $variableContainer: VariableProviderInterface
        :param $variableContainer:
        :returns: void
