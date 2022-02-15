-------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\SectionViewHelper
-------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: SectionViewHelper

    A ViewHelper to declare sections in templates for later use with e.g. the ``f:render`` ViewHelper.

    Examples
    ========

    Rendering sections
    ------------------

    ::

        <f:section name="someSection">This is a section. {foo}</f:section>
        <f:render section="someSection" arguments="{foo: someVariable}" />

    Output::

        the content of the section "someSection". The content of the variable {someVariable} will be available in the partial as {foo}

    Rendering recursive sections
    ----------------------------

    ::

        <f:section name="mySection">
           <ul>
                <f:for each="{myMenu}" as="menuItem">
                     <li>
                       {menuItem.text}
                       <f:if condition="{menuItem.subItems}">
                           <f:render section="mySection" arguments="{myMenu: menuItem.subItems}" />
                       </f:if>
                     </li>
                </f:for>
           </ul>
        </f:section>
        <f:render section="mySection" arguments="{myMenu: menu}" />

    Output::

        <ul>
            <li>menu1
                <ul>
                    <li>menu1a</li>
                    <li>menu1b</li>
                </ul>
            </li>
        [...]
        (depending on the value of {menu})

    .. php:attr:: escapeOutput

        protected boolean

    .. php:method:: initializeArguments()

        Initialize the arguments.

        :returns: void

    .. php:method:: postParseEvent(ViewHelperNode $node, $arguments, VariableProviderInterface $variableContainer)

        Save the associated ViewHelper node in a static public class variable.
        called directly after the ViewHelper was built.

        :type $node: ViewHelperNode
        :param $node:
        :type $arguments: TextNode[]
        :param $arguments:
        :type $variableContainer: VariableProviderInterface
        :param $variableContainer:
        :returns: void

    .. php:method:: render()

        Rendering directly returns all child nodes.

        :returns: string HTML String of all child nodes.
