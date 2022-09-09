.. Copyright (c) 2022 Digital Asset (Switzerland) GmbH and/or its affiliates. All rights reserved.
.. SPDX-License-Identifier: Apache-2.0

.. _module-daml-finance-interface-holding-base-24195:

Module Daml.Finance.Interface.Holding.Base
==========================================

Interfaces
----------

.. _type-daml-finance-interface-holding-base-base-14854:

**interface** `Base <type-daml-finance-interface-holding-base-base-14854_>`_

  Base interface for a holding\.
  
  **viewtype** `V <type-daml-finance-interface-holding-base-v-39458_>`_
  
  + **Choice GetView**
    
    Retrieves the interface view\.
    
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - viewer
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - The party retrieving the view\.
  
  + **Method asDisclosure \:** :ref:`I <type-daml-finance-interface-util-disclosure-i-26993>`
    
    Conversion to ``Disclosure`` interface\.

Typeclasses
-----------

.. _class-daml-finance-interface-holding-base-hasimplementation-31795:

**class** `Implementation <type-daml-finance-interface-holding-base-implementation-87781_>`_ t \=\> `HasImplementation <class-daml-finance-interface-holding-base-hasimplementation-31795_>`_ t **where**


Data Types
----------

.. _type-daml-finance-interface-holding-base-i-67605:

**type** `I <type-daml-finance-interface-holding-base-i-67605_>`_
  \= `Base <type-daml-finance-interface-holding-base-base-14854_>`_
  
  Type synonym for ``Base``\.
  
  **instance** HasMethod :ref:`Account <type-daml-finance-interface-holding-account-account-25212>` \"credit\" (Credit \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `I <type-daml-finance-interface-holding-base-i-67605_>`_))
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-holding-factory-holding-factory-29039>` \"create'\" (Create \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `I <type-daml-finance-interface-holding-base-i-67605_>`_))
  
  **instance** HasMethod :ref:`Lockable <type-daml-finance-interface-holding-lockable-lockable-97810>` \"asHolding\" `I <type-daml-finance-interface-holding-base-i-67605_>`_

.. _type-daml-finance-interface-holding-base-implementation-87781:

**type** `Implementation <type-daml-finance-interface-holding-base-implementation-87781_>`_ t
  \= (`HasToInterface <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-interface-hastointerface-68104>`_ t `I <type-daml-finance-interface-holding-base-i-67605_>`_, :ref:`Implementation <type-daml-finance-interface-util-disclosure-implementation-41553>` t)
  
  Type constraint for requiring templates to implement ``Holding`` along with ``Disclosure``\.

.. _type-daml-finance-interface-holding-base-v-39458:

**type** `V <type-daml-finance-interface-holding-base-v-39458_>`_
  \= `View <type-daml-finance-interface-holding-base-view-44702_>`_
  
  Type synonym for ``View``\.

.. _type-daml-finance-interface-holding-base-view-44702:

**data** `View <type-daml-finance-interface-holding-base-view-44702_>`_

  View for ``Base``\.
  
  .. _constr-daml-finance-interface-holding-base-view-84815:
  
  `View <constr-daml-finance-interface-holding-base-view-84815_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - instrument
         - :ref:`InstrumentKey <type-daml-finance-interface-types-common-instrumentkey-59982>`
         - Instrument being held\.
       * - account
         - :ref:`AccountKey <type-daml-finance-interface-types-common-accountkey-85835>`
         - Key of the account holding the assets\.
       * - amount
         - `Decimal <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-decimal-18135>`_
         - Size of the holding\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `View <type-daml-finance-interface-holding-base-view-44702_>`_
  
  **instance** `Ord <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-ord-6395>`_ `View <type-daml-finance-interface-holding-base-view-44702_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `View <type-daml-finance-interface-holding-base-view-44702_>`_

Functions
---------

.. _function-daml-finance-interface-holding-base-asdisclosure-65162:

`asDisclosure <function-daml-finance-interface-holding-base-asdisclosure-65162_>`_
  \: `Base <type-daml-finance-interface-holding-base-base-14854_>`_ \-\> :ref:`I <type-daml-finance-interface-util-disclosure-i-26993>`
