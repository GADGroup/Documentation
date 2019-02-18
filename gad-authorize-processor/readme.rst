=========================
gad_authorize_processor
=========================

Installation
============

* Install  this module in a usual way

Configuration
=============

| **Once the module is installed**, add a user to modules "Manager" group!
| Then visit -> ``GAD Authorize.NET`` -> ``Payment Acquirers`` -> ``Authorize.NET``

Here you will see a new tab "GAD Authorize Settings" in here we have two tables of options.

| **Payment Settings**: Contains general applications settings.

:key: ``Re Authorize Card Days``
:value: ``Integer``
:description: ``Days before authorized transaction is voided and re-authorized.``

:key: ``Email Re-Authorization Failure``
:value: ``Char``
:description: ``Email address used to send re-authorization failure message.``

| **Company Credentials**: Contains Authorize.NET credentials for multiple companies within Odoo.

| - Add your ``Authorize.NET`` credentials here for each company.
| - If no additonal credentials are added for a company within Odoo
 the default Authorize.NET credentials are used.
| - Each record must have unique ``company``

Usage
==========

| **Sales Order**
| - [**Accept Card (Executable by User/Manager Group)**]
|  1. Enter amount and new card details or choose an existing card.
|  2. (Create Token) Generates ``Authorize.NET`` Profile Token
      and creates an Authorization Token on provided card.
| - [**Transactions Smart Button**]
|  1. Click to view all transaction related to current sales order.
|  2. Can view transaction and "Void Payment"(Manager Group) here if necessary.

| **Invoice**
| - [**Capture Payment  (Executable by Manager Group)**]
|  1. Choose transaction from drop-down.
|  2. Choose Journal to attach payment to.
|  3. Choose payment method. (eg Electronic)
|  4. (Capture Payment) Captures a previously authorized
    charge. Creates an account.payment record and journal entry.
|  5. [OR] (Void Payment) Voids a previously authorized charge.

| **GAD Authorize.NET/Logs (Viewable by User/Manager Group)**
| - Contains logs of Authorize.NET activity.

Notes
======
.. warning:: If Company of Sales Order does not have credentials in settings
  the module will use default Authorize.NET credentials.

- If payment credentials are not accepted a message will be displayed with the reason why.
- Re Authorize Days defaults to 5 / Change default email message address
- Receive email & message in General Chat when re authorization. If no outgoing mail server isn't
  set just chat message will be received.


Help / Contact Us
=================
- http://www.GADGroup.com
- support@gadgroup.com

Feel free to contact us for anything!

This application is not endorsed by, directly affiliated with, maintained, authorized,
or sponsored by any company outside of GADGroup Technology, Inc. All product and company names
are the registered trademarks of their original owners. The use of any trade name or trademark is
for identification and reference purposes only and does not imply any association with the
trademark holder of their product brand.
