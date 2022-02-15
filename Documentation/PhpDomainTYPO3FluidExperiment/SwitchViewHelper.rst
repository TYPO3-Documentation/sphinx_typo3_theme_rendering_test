------------------------------------------------
TYPO3Fluid\\Fluid\\ViewHelpers\\SwitchViewHelper
------------------------------------------------

.. php:namespace: TYPO3Fluid\\Fluid\\ViewHelpers

.. php:class:: SwitchViewHelper

    Switch ViewHelper which can be used to render content depending on a value or expression.
    Implements what a basic PHP ``switch()`` does.

    An optional default case can be specified which is rendered if none of the
    ``case`` conditions matches.

    Using this ViewHelper can be a sign of weak architecture. If you end up using it extensively you might want to consider restructuring your controllers/actions and/or use partials and sections.
    E.g. the above example could be achieved with :html:`<f:render partial="title.{person.gender}" />`
    and the partials "title.male.html", "title.female.html", ...
    Depending on the scenario this can be easier to extend and possibly contains less duplication.

    Examples
    ========

    Simple Switch statement
    -----------------------

    ::

        <f:switch expression="{person.gender}">
            <f:case value="male">Mr.</f:case>
            <f:case value="female">Mrs.</f:case>
            <f:defaultCase>Mr. / Mrs.</f:defaultCase>
        </f:switch>

    Output::

        "Mr.", "Mrs." or "Mr. / Mrs." (depending on the value of {person.gender})

    .. php:attr:: escapeOutput

        protected boolean

    .. php:attr:: backupSwitchExpression

        protected mixed

    .. php:attr:: backupBreakState

        protected boolean

    .. php:method:: initializeArguments()

        :returns: void

    .. php:method:: render()

        :returns: string the rendered string

    .. php:method:: retrieveContentFromChildNodes($childNodes)

        :type $childNodes: NodeInterface[]
        :param $childNodes:
        :returns: mixed

    .. php:method:: isDefaultCaseNode(NodeInterface $node)

        :type $node: NodeInterface
        :param $node:
        :returns: boolean

    .. php:method:: isCaseNode(NodeInterface $node)

        :type $node: NodeInterface
        :param $node:
        :returns: boolean

    .. php:method:: backupSwitchState()

        Backups "switch expression" and "break" state of a possible parent switch
        ViewHelper to support nesting

        :returns: void

    .. php:method:: restoreSwitchState()

        Restores "switch expression" and "break" states that might have been
        backed up in backupSwitchState() before

        :returns: void

    .. php:method:: compile($argumentsName, $closureName, $initializationPhpCode, ViewHelperNode $node, TemplateCompiler $compiler)

        Compiles the node structure to a native switch
        statement which evaluates closures for each
        case comparison and renders child node closures
        only when value matches.

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
