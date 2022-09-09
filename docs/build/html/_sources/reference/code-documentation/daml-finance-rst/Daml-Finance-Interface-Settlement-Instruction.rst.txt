.. Copyright (c) 2022 Digital Asset (Switzerland) GmbH and/or its affiliates. All rights reserved.
.. SPDX-License-Identifier: Apache-2.0

.. _module-daml-finance-interface-settlement-instruction-10970:

Module Daml.Finance.Interface.Settlement.Instruction
====================================================

Interfaces
----------

.. _type-daml-finance-interface-settlement-instruction-instruction-30569:

**interface** `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_

  An interface for providing a single instruction to transfer an asset\.
  
  **viewtype** `V <type-daml-finance-interface-settlement-instruction-v-83729_>`_
  
  + **Choice Allocate**
    
    Allocate an asset to an instruction\.
    
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - allocation
         - :ref:`Allocation <type-daml-finance-interface-settlement-types-allocation-46483>`
         - Allocation of an instruction\.
  
  + **Choice Approve**
    
    Approve this instruction\.
    
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - approval
         - :ref:`Approval <type-daml-finance-interface-settlement-types-approval-84286>`
         - Approval of an instruction\.
  
  + **Choice Execute**
    
    Execute the instruction\.
    
  
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
  
  + **Method allocate \:** Allocate \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_)
    
    Implementation of the ``Allocate`` choice\.
  
  + **Method approve \:** Approve \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_)
    
    Implementation of the ``Approve`` choice\.
  
  + **Method asDisclosure \:** :ref:`I <type-daml-finance-interface-util-disclosure-i-26993>`
    
    Conversion to ``Disclosure`` interface\.
  
  + **Method execute \:** `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`Optional <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-prelude-optional-37153>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`I <type-daml-finance-interface-holding-transferable-i-13335>`))
    
    Implementation of the ``Execute`` choice\.

Typeclasses
-----------

.. _class-daml-finance-interface-settlement-instruction-hasimplementation-40548:

**class** `Implementation <type-daml-finance-interface-settlement-instruction-implementation-17580_>`_ t \=\> `HasImplementation <class-daml-finance-interface-settlement-instruction-hasimplementation-40548_>`_ t **where**


Data Types
----------

.. _type-daml-finance-interface-settlement-instruction-i-90342:

**type** `I <type-daml-finance-interface-settlement-instruction-i-90342_>`_
  \= `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_
  
  Type synonym for ``Instruction``\.
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-settlement-factory-factory-31525>` \"instruct\" (Instruct \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`I <type-daml-finance-interface-settlement-batch-i-3768>`, \[`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `I <type-daml-finance-interface-settlement-instruction-i-90342_>`_\]))

.. _type-daml-finance-interface-settlement-instruction-implementation-17580:

**type** `Implementation <type-daml-finance-interface-settlement-instruction-implementation-17580_>`_ t
  \= (`HasToInterface <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-interface-hastointerface-68104>`_ t `I <type-daml-finance-interface-settlement-instruction-i-90342_>`_, :ref:`Implementation <type-daml-finance-interface-util-disclosure-implementation-41553>` t)
  
  Type constraint for requiring templates to implement ``Instruction`` along with ``Disclosure``\.

.. _type-daml-finance-interface-settlement-instruction-v-83729:

**type** `V <type-daml-finance-interface-settlement-instruction-v-83729_>`_
  \= `View <type-daml-finance-interface-settlement-instruction-view-45863_>`_
  
  Type synonym for ``View``\.

.. _type-daml-finance-interface-settlement-instruction-view-45863:

**data** `View <type-daml-finance-interface-settlement-instruction-view-45863_>`_

  View for ``Instruction``\.
  
  .. _constr-daml-finance-interface-settlement-instruction-view-23498:
  
  `View <constr-daml-finance-interface-settlement-instruction-view-23498_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - settler
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - Party which execute the Instruction\.
       * - step
         - :ref:`Step <type-daml-finance-interface-settlement-types-step-78661>`
         - Instruction details to execute\.
       * - id
         - :ref:`Id <type-daml-finance-interface-types-common-id-56542>`
         - Instruction identifier\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `View <type-daml-finance-interface-settlement-instruction-view-45863_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `View <type-daml-finance-interface-settlement-instruction-view-45863_>`_

Functions
---------

.. _function-daml-finance-interface-settlement-instruction-asdisclosure-49219:

`asDisclosure <function-daml-finance-interface-settlement-instruction-asdisclosure-49219_>`_
  \: `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_ \-\> :ref:`I <type-daml-finance-interface-util-disclosure-i-26993>`

.. _function-daml-finance-interface-settlement-instruction-allocate-71473:

`allocate <function-daml-finance-interface-settlement-instruction-allocate-71473_>`_
  \: `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_ \-\> Allocate \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_)

.. _function-daml-finance-interface-settlement-instruction-approve-37030:

`approve <function-daml-finance-interface-settlement-instruction-approve-37030_>`_
  \: `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_ \-\> Approve \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_)

.. _function-daml-finance-interface-settlement-instruction-execute-46460:

`execute <function-daml-finance-interface-settlement-instruction-execute-46460_>`_
  \: `Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569_>`_ \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`Optional <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-prelude-optional-37153>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`I <type-daml-finance-interface-holding-transferable-i-13335>`))
