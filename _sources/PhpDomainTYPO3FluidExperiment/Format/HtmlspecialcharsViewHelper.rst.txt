------------------------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\Format\\HtmlspecialcharsViewHelper
------------------------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers\\Format

.. php:class:: HtmlspecialcharsViewHelper

    Applies PHP ``htmlspecialchars()`` escaping to a value.

    See http://www.php.net/manual/function.htmlspecialchars.php

    Examples
    ========

    Default notation
    ----------------

    ::

        <f:format.htmlspecialchars>{text}</f:format.htmlspecialchars>

    Output::

        Text with & " ' < > * replaced by HTML entities (htmlspecialchars applied).

    Inline notation
    ---------------

    ::

        {text -> f:format.htmlspecialchars(encoding: 'ISO-8859-1')}

    Output::

        Text with & " ' < > * replaced by HTML entities (htmlspecialchars applied).

    .. php:attr:: escapeChildren

        protected boolean

    .. php:attr:: escapeOutput

        protected boolean

        Disable the output escaping interceptor so that the value is not
        htmlspecialchar'd twice

    .. php:method:: initializeArguments()

        :returns: void

    .. php:method:: render()

        Escapes special characters with their escaped counterparts as needed using
        PHPs htmlspecialchars() function.

        :returns: string the altered string

    .. php:method:: compile($argumentsName, $closureName, $initializationPhpCode, ViewHelperNode $node, TemplateCompiler $compiler)

        This ViewHelper is used a *lot* because it is used by the escape
        interceptor.
        Therefore we render it to raw PHP code during compilation

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
