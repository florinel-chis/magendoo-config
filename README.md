magendoo-config
===============

Improved error message in Magento Configuration


*Issue*

Magento Config controller makes the follwing checks:
* the config section is defined in ACL - if not, Magento will display a 404, nothing helpful
* the user is allowed to access that resource - displays the denied action page
* most times I don't add the ACL when defining a new config section and Magento doesn't spell out what is wrong, so I waste some time debugging

Note: Magento's ACL data is stored in session (after changes make sure you clear your session)

*What I did*

Override Mage_Adminhtml_System_ConfigController in order to display a clear error message about what should I do.

*Feedback*

Feedback/improvments are always welcome. Thanks.