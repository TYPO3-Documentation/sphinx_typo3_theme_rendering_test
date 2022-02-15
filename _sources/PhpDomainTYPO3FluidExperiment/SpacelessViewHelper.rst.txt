---------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\SpacelessViewHelper
---------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: SpacelessViewHelper

    Space Removal ViewHelper

    Removes redundant spaces between HTML tags while preserving the whitespace that may be inside HTML tags. Trims the final result before output.

    Heavily inspired by Twig's corresponding node type.

    Usage of f:spaceless
    ====================

    ::

        <f:spaceless>
            <div>
                <div>
                    <div>text

            text</div>
                </div>
            </div>
        </f:spaceless>

    Output::

        <div><div><div>text

        text</div></div></div>

    .. php:attr:: escapeOutput

        protected boolean

    .. php:method:: renderStatic($arguments, Closure $childClosure, RenderingContextInterface $renderingContext)

        :type $arguments: array
        :param $arguments:
        :type $childClosure: Closure
        :param $childClosure:
        :type $renderingContext: RenderingContextInterface
        :param $renderingContext:
        :returns: string
