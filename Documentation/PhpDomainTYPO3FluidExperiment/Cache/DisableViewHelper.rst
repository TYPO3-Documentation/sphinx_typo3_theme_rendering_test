--------------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\Cache\\DisableViewHelper
--------------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers\\Cache

.. php:class:: DisableViewHelper

    ViewHelper to disable template compiling

    Inserting this ViewHelper at any point in the template,
    including inside conditions which do not get rendered,
    will forcibly disable the caching/compiling of the full template file to a PHP class.

    Use this if for whatever reason your platform is unable to create or load PHP classes (for example on read-only file systems or when using an incompatible default cache backend).

    Passes through anything you place inside the ViewHelper,
    so can safely be used as container tag, as self-closing or with inline syntax - all with the same result.

    Examples
    ========

    Self-closing
    ------------

    ::

        <f:cache.disable />

    Inline mode
    -----------

    ::

        {f:cache.disable()}

    Container tag
    -------------

    ::

        <f:cache.disable>
           Some output or Fluid code
        </f:cache.disble>

    Additional output is also not compilable because of the ViewHelper

    .. php:attr:: escapeChildren

        protected boolean

    .. php:attr:: escapeOutput

        protected boolean

    .. php:method:: render()

        :returns: string

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
