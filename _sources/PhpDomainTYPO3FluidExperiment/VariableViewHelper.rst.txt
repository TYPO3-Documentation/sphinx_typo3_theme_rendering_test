--------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\VariableViewHelper
--------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: VariableViewHelper

    Variable assigning ViewHelper

    Assigns one template variable which will exist also after the ViewHelper is done rendering, i.e. adds template variables.

    If you require a variable assignment which does not exist in the template after a piece of Fluid code is rendered, consider using ``f:alias`` ViewHelper instead.

    Usages:

    ::

        {f:variable(name: 'myvariable', value: 'some value')}
        <f:variable name="myvariable">some value</f:variable>
        {oldvariable -> f:format.htmlspecialchars() -> f:variable(name: 'newvariable')}
        <f:variable name="myvariable"><f:format.htmlspecialchars>{oldvariable}</f:format.htmlspecialchars></f:variable>

    .. php:method:: initializeArguments()

        :returns: void

    .. php:method:: renderStatic($arguments, Closure $renderChildrenClosure, RenderingContextInterface $renderingContext)

        :type $arguments: array
        :param $arguments:
        :type $renderChildrenClosure: Closure
        :param $renderChildrenClosure:
        :type $renderingContext: RenderingContextInterface
        :param $renderingContext:
        :returns: null
