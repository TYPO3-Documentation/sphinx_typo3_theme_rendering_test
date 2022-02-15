---------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\ForViewHelper
---------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: ForViewHelper

    Loop ViewHelper which can be used to iterate over arrays.
    Implements what a basic PHP ``foreach()`` does.

    Examples
    ========

    Simple Loop
    -----------

    ::

        <f:for each="{0:1, 1:2, 2:3, 3:4}" as="foo">{foo}</f:for>

    Output::

        1234

    Output array key
    ----------------

    ::

        <ul>
            <f:for each="{fruit1: 'apple', fruit2: 'pear', fruit3: 'banana', fruit4: 'cherry'}"
                as="fruit" key="label"
            >
                <li>{label}: {fruit}</li>
            </f:for>
        </ul>

    Output::

        <ul>
            <li>fruit1: apple</li>
            <li>fruit2: pear</li>
            <li>fruit3: banana</li>
            <li>fruit4: cherry</li>
        </ul>

    Iteration information
    ---------------------

    ::

        <ul>
            <f:for each="{0:1, 1:2, 2:3, 3:4}" as="foo" iteration="fooIterator">
                <li>Index: {fooIterator.index} Cycle: {fooIterator.cycle} Total: {fooIterator.total}{f:if(condition: fooIterator.isEven, then: ' Even')}{f:if(condition: fooIterator.isOdd, then: ' Odd')}{f:if(condition: fooIterator.isFirst, then: ' First')}{f:if(condition: fooIterator.isLast, then: ' Last')}</li>
            </f:for>
        </ul>

    Output::

        <ul>
            <li>Index: 0 Cycle: 1 Total: 4 Odd First</li>
            <li>Index: 1 Cycle: 2 Total: 4 Even</li>
            <li>Index: 2 Cycle: 3 Total: 4 Odd</li>
            <li>Index: 3 Cycle: 4 Total: 4 Even Last</li>
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
        :returns: string
