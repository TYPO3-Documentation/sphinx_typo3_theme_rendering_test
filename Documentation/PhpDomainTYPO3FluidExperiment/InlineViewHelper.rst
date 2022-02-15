------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\InlineViewHelper
------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: InlineViewHelper

    Inline Fluid rendering ViewHelper

    Renders Fluid code stored in a variable, which you normally would have to render before assigning it to the view. Instead you can do the following (note, extremely simplified use case)::

         $view->assign('variable', 'value of my variable');
         $view->assign('code', 'My variable: {variable}');

    And in the template::

         {code -> f:inline()}

    Which outputs::

         My variable: value of my variable

    You can use this to pass smaller and dynamic pieces of Fluid code to templates, as an alternative to creating new partial templates.

    .. php:attr:: escapeChildren

        protected

    .. php:attr:: escapeOutput

        protected

    .. php:method:: initializeArguments()

        :returns: void

    .. php:method:: renderStatic($arguments, Closure $renderChildrenClosure, RenderingContextInterface $renderingContext)

        :type $arguments: array
        :param $arguments:
        :type $renderChildrenClosure: Closure
        :param $renderChildrenClosure:
        :type $renderingContext: RenderingContextInterface
        :param $renderingContext:
        :returns: mixed|string
