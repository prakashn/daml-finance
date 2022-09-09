.. Copyright (c) 2022 Digital Asset (Switzerland) GmbH and/or its affiliates. All rights reserved.
.. SPDX-License-Identifier: Apache-2.0

.. _module-daml-finance-interface-settlement-batch-39188:

Module Daml.Finance.Interface.Settlement.Batch
==============================================

Interfaces
----------

.. _type-daml-finance-interface-settlement-batch-batch-97497:

**interface** `Batch <type-daml-finance-interface-settlement-batch-batch-97497_>`_

  An interface for atomically settling ``Transferable``\\s\.
  
  **viewtype** `V <type-daml-finance-interface-settlement-batch-v-79775_>`_
  
  + **Choice GetView**
    
    Retrieves the instrument view\.
    
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - viewer
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - The party retrieving the view\.
  
  + **Choice Settle**
    
    Execute settlement\.
    
  
  + **Method settle \:** `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ \[`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`I <type-daml-finance-interface-holding-transferable-i-13335>`\]
    
    Implementation of the ``Settle`` choice\.

Typeclasses
-----------

.. _class-daml-finance-interface-settlement-batch-hasimplementation-10022:

**class** `Implementation <type-daml-finance-interface-settlement-batch-implementation-59610_>`_ t \=\> `HasImplementation <class-daml-finance-interface-settlement-batch-hasimplementation-10022_>`_ t **where**


Data Types
----------

.. _type-daml-finance-interface-settlement-batch-i-3768:

**type** `I <type-daml-finance-interface-settlement-batch-i-3768_>`_
  \= `Batch <type-daml-finance-interface-settlement-batch-batch-97497_>`_
  
  Type synonym for ``Batch``\.
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-settlement-factory-factory-31525>` \"instruct\" (Instruct \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `I <type-daml-finance-interface-settlement-batch-i-3768_>`_, \[`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`I <type-daml-finance-interface-settlement-instruction-i-90342>`\]))

.. _type-daml-finance-interface-settlement-batch-implementation-59610:

**type** `Implementation <type-daml-finance-interface-settlement-batch-implementation-59610_>`_ t
  \= `HasToInterface <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-interface-hastointerface-68104>`_ t `I <type-daml-finance-interface-settlement-batch-i-3768_>`_
  
  Type constraint for requiring templates to implement ``Batch``\.

.. _type-daml-finance-interface-settlement-batch-v-79775:

**type** `V <type-daml-finance-interface-settlement-batch-v-79775_>`_
  \= `View <type-daml-finance-interface-settlement-batch-view-33973_>`_
  
  Type synonym for ``View``\.

.. _type-daml-finance-interface-settlement-batch-view-33973:

**data** `View <type-daml-finance-interface-settlement-batch-view-33973_>`_

  View for ``Batch``\.
  
  .. _constr-daml-finance-interface-settlement-batch-view-72084:
  
  `View <constr-daml-finance-interface-settlement-batch-view-72084_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - settler
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - Party triggering the settlement\.
       * - steps
         - \[:ref:`Step <type-daml-finance-interface-settlement-types-step-78661>`\]
         - Settlement steps\.
       * - id
         - :ref:`Id <type-daml-finance-interface-types-common-id-56542>`
         - Batch identifier\.
       * - description
         - `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
         - Batch description\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `View <type-daml-finance-interface-settlement-batch-view-33973_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `View <type-daml-finance-interface-settlement-batch-view-33973_>`_

Functions
---------

.. _function-daml-finance-interface-settlement-batch-settle-40325:

`settle <function-daml-finance-interface-settlement-batch-settle-40325_>`_
  \: `Batch <type-daml-finance-interface-settlement-batch-batch-97497_>`_ \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ \[`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`I <type-daml-finance-interface-holding-transferable-i-13335>`\]
