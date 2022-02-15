-----------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\CycleViewHelper
-----------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: CycleViewHelper

    This ViewHelper cycles through the specified values.
    This can be often used to specify CSS classes for example.

    To achieve the "zebra class" effect in a loop you can also use the
    "iteration" argument of the **for** ViewHelper.

    Examples
    ========

    These examples could also be achieved using the "iteration" argument of the ForViewHelper.

    Simple
    ------

    ::

        <f:for each="{0:1, 1:2, 2:3, 3:4}" as="foo">
            <f:cycle values="{0: 'foo', 1: 'bar', 2: 'baz'}" as="cycle">
                {cycle}
            </f:cycle>
        </f:for>

    Output::

        foobarbazfoo

    Alternating CSS class
    ---------------------

    ::

        <ul>
            <f:for each="{0:1, 1:2, 2:3, 3:4}" as="foo">
                <f:cycle values="{0: 'odd', 1: 'even'}" as="zebraClass">
                    <li class="{zebraClass}">{foo}</li>
                </f:cycle>
            </f:for>
        </ul>

    Output::

        <ul>
            <li class="odd">1</li>
            <li class="even">2</li>
            <li class="odd">3</li>
            <li class="even">4</li>
        </ul>

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

    .. php:method:: initializeValues($values)

        :type $values: mixed
        :param $values:
        :returns: array

    .. php:method:: initializeIndex($as, ViewHelper\ViewHelperVariableContainer $viewHelperVariableContainer)

        :type $as: string
        :param $as:
        :type $viewHelperVariableContainer: ViewHelper\ViewHelperVariableContainer
        :param $viewHelperVariableContainer:
        :returns: integer
