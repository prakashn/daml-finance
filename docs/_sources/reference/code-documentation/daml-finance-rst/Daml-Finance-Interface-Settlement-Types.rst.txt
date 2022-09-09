.. Copyright (c) 2022 Digital Asset (Switzerland) GmbH and/or its affiliates. All rights reserved.
.. SPDX-License-Identifier: Apache-2.0

.. _module-daml-finance-interface-settlement-types-44085:

Module Daml.Finance.Interface.Settlement.Types
==============================================

Data Types
----------

.. _type-daml-finance-interface-settlement-types-allocation-46483:

**data** `Allocation <type-daml-finance-interface-settlement-types-allocation-46483_>`_

  Describes an allocation of an ``Instruction``\.
  
  .. _constr-daml-finance-interface-settlement-types-unallocated-82559:
  
  `Unallocated <constr-daml-finance-interface-settlement-types-unallocated-82559_>`_
  
    An unallocated instruction\.
  
  .. _constr-daml-finance-interface-settlement-types-pledge-99803:
  
  `Pledge <constr-daml-finance-interface-settlement-types-pledge-99803_>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`I <type-daml-finance-interface-holding-transferable-i-13335>`)
  
    Settle the instruction with the pledged asset\.
  
  .. _constr-daml-finance-interface-settlement-types-creditreceiver-50700:
  
  `CreditReceiver <constr-daml-finance-interface-settlement-types-creditreceiver-50700_>`_
  
    Settle the instruction by crediting the receiver account (where the sender is custodian)\.
  
  .. _constr-daml-finance-interface-settlement-types-settleoffledger-89308:
  
  `SettleOffLedger <constr-daml-finance-interface-settlement-types-settleoffledger-89308_>`_
  
    Settle the instruction offledger\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `Allocation <type-daml-finance-interface-settlement-types-allocation-46483_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `Allocation <type-daml-finance-interface-settlement-types-allocation-46483_>`_

.. _type-daml-finance-interface-settlement-types-approval-84286:

**data** `Approval <type-daml-finance-interface-settlement-types-approval-84286_>`_

  Describes an approval of an ``Instruction``\.
  
  .. _constr-daml-finance-interface-settlement-types-unapproved-57468:
  
  `Unapproved <constr-daml-finance-interface-settlement-types-unapproved-57468_>`_
  
    An unapproved instruction\.
  
  .. _constr-daml-finance-interface-settlement-types-takedelivery-14079:
  
  `TakeDelivery <constr-daml-finance-interface-settlement-types-takedelivery-14079_>`_ :ref:`AccountKey <type-daml-finance-interface-types-common-accountkey-85835>`
  
    Take delivery to the specified account\.
  
  .. _constr-daml-finance-interface-settlement-types-debitsender-39086:
  
  `DebitSender <constr-daml-finance-interface-settlement-types-debitsender-39086_>`_
  
    Approve the instruction by debiting the sender account with the provided asset (where the receiver is custodian)\.
  
  .. _constr-daml-finance-interface-settlement-types-settleoffledgeracknowledge-30301:
  
  `SettleOffLedgerAcknowledge <constr-daml-finance-interface-settlement-types-settleoffledgeracknowledge-30301_>`_
  
    Acknowledge settlement of the instruction offledger\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `Approval <type-daml-finance-interface-settlement-types-approval-84286_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `Approval <type-daml-finance-interface-settlement-types-approval-84286_>`_

.. _type-daml-finance-interface-settlement-types-step-78661:

**data** `Step <type-daml-finance-interface-settlement-types-step-78661_>`_

  Describes a transfer of a position between two parties\.
  
  .. _constr-daml-finance-interface-settlement-types-step-97764:
  
  `Step <constr-daml-finance-interface-settlement-types-step-97764_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - sender
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - Party transferring the asset\.
       * - receiver
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - Party receiving the asset\.
       * - quantity
         - :ref:`Q <type-daml-finance-interface-instrument-base-instrument-q-62956>`
         - The instrument and amount to be transferred\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `Step <type-daml-finance-interface-settlement-types-step-78661_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `Step <type-daml-finance-interface-settlement-types-step-78661_>`_
