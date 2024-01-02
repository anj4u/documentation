==================
Internal transfers
==================

Internal money transfers can be handled in Odoo. At least two bank accounts are needed to make
internal transfers.

.. seealso::
   :doc:`How to add an additional bank account <../bank>`

Configuration
=============

An internal transfer account is automatically created on your database based on your company's
localization and depending on your country’s legislation. To modify the default :guilabel:`Internal
transfer account`, go to :menuselection:`Accounting --> Configuration --> Settings` and scroll down
to the :guilabel:`Default Accounts` section.

Register an internal transfer from one bank to another
======================================================

Log an internal transfer
------------------------

If you want to transfer money from one bak to another, access the Accounting Dashboard, click the
drop-down selection button (:guilabel:`⋮`) on the bank from which you want to make the transfer,
then click :guilabel:`Payments`. Select or create a payment, tick the :guilabel:`Internal Transfer`
checkbox, and select :guilabel:`Destination Journal` before you :guilabel:`Confirm` the internal
transfer.

The money is now booked in the transfer account and another payment is automatically created in the
destination journal. Reconciling internal transfers is the same process as other bank transfers.

.. example::

   - Bank journal (Bank A)

     .. list-table::
        :header-rows: 1
        :stub-columns: 1

        * - **Account**
          - **Debit**
          - **Credit**
        * - Outstanding Payments account
          -
          - $1,000
        * - **Internal transfer account**
          - **$1,000**
          -

   - Bank journal (Bank B)


     .. list-table::
        :header-rows: 1
        :stub-columns: 1

        * - **Account**
          - **Debit**
          - **Credit**
        * - Outstanding Receipts account
          - $1,000
          -
        * - **Internal transfer account**
          -
          - **$1,000**

   There is **one outstanding payment** and **one outstanding receipt** pending in your two bank
   account journals, because the bank statement confirming the sending and receiving of the money
   has not been booked yet.

   The same steps must be **repeated** once you receive the bank statement related to **Bank B**.
   Book and reconcile your bank statement lines.

.. seealso::
   :doc:`../bank/reconciliation`
