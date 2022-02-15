----------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\GroupedForViewHelper
----------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: GroupedForViewHelper

    Grouped loop ViewHelper.
    Loops through the specified values.

    The groupBy argument also supports property paths.

    Using this ViewHelper can be a sign of weak architecture. If you end up using it extensively you might want to fine-tune your "view model" (the data you assign to the view).

    Examples
    ========

    Simple
    ------

    ::

        <f:groupedFor each="{0: {name: 'apple', color: 'green'}, 1: {name: 'cherry', color: 'red'}, 2: {name: 'banana', color: 'yellow'}, 3: {name: 'strawberry', color: 'red'}}"
            as="fruitsOfThisColor" groupBy="color"
        >
            <f:for each="{fruitsOfThisColor}" as="fruit">
                {fruit.name}
            </f:for>
        </f:groupedFor>

    Output::

        apple cherry strawberry banana

    Two dimensional list
    --------------------

    ::

        <ul>
            <f:groupedFor each="{0: {name: 'apple', color: 'green'}, 1: {name: 'cherry', color: 'red'}, 2: {name: 'banana', color: 'yellow'}, 3: {name: 'strawberry', color: 'red'}}" as="fruitsOfThisColor" groupBy="color" groupKey="color">
                <li>
                    {color} fruits:
                    <ul>
                        <f:for each="{fruitsOfThisColor}" as="fruit" key="label">
                            <li>{label}: {fruit.name}</li>
                        </f:for>
                    </ul>
                </li>
            </f:groupedFor>
        </ul>

    Output::

        <ul>
            <li>green fruits
                <ul>
                    <li>0: apple</li>
                </ul>
            </li>
            <li>red fruits
                <ul>
                    <li>1: cherry</li>
                </ul>
                <ul>
                    <li>3: strawberry</li>
                </ul>
            </li>
            <li>yellow fruits
                <ul>
                    <li>2: banana</li>
                </ul>
            </li>
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

    .. php:method:: groupElements($elements, $groupBy)

        Groups the given array by the specified groupBy property.

        :type $elements: array
        :param $elements: The array / traversable object to be grouped
        :type $groupBy: string
        :param $groupBy: Group by this property
        :returns: array The grouped array in the form array('keys' => array('key1' => [key1value], 'key2' => [key2value], ...), 'values' => array('key1' => array([key1value] => [element1]), ...), ...)
