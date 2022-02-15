--------------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\Format\\PrintfViewHelper
--------------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers\\Format

.. php:class:: PrintfViewHelper

    A ViewHelper for formatting values with printf. Either supply an array for
    the arguments or a single value.

    See http://www.php.net/manual/en/function.sprintf.php

    Examples
    ========

    Scientific notation
    -------------------

    ::

        <f:format.printf arguments="{number: 362525200}">%.3e</f:format.printf>

    Output::

        3.625e+8

    Argument swapping
    -----------------

    ::

        <f:format.printf arguments="{0: 3, 1: 'Kasper'}">%2$s is great, TYPO%1$d too. Yes, TYPO%1$d is great and so is %2$s!</f:format.printf>

    Output::

        Kasper is great, TYPO3 too. Yes, TYPO3 is great and so is Kasper!

    Single argument
    ---------------

    ::

        <f:format.printf arguments="{1: 'TYPO3'}">We love %s</f:format.printf>

    Output::

        We love TYPO3

    Inline notation
    ---------------

    ::

        {someText -> f:format.printf(arguments: {1: 'TYPO3'})}

    Output::

        We love TYPO3

    .. php:method:: initializeArguments()

        :returns: void

    .. php:method:: renderStatic($arguments, Closure $renderChildrenClosure, RenderingContextInterface $renderingContext)

        Applies vsprintf() on the specified value.

        :type $arguments: array
        :param $arguments:
        :type $renderChildrenClosure: Closure
        :param $renderChildrenClosure:
        :type $renderingContext: RenderingContextInterface
        :param $renderingContext:
        :returns: string
