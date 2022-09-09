.. Copyright (c) 2022 Digital Asset (Switzerland) GmbH and/or its affiliates. All rights reserved.
.. SPDX-License-Identifier: Apache-2.0

.. _module-daml-finance-interface-util-disclosure-87755:

Module Daml.Finance.Interface.Util.Disclosure
=============================================

Interfaces
----------

.. _type-daml-finance-interface-util-disclosure-disclosure-97052:

**interface** `Disclosure <type-daml-finance-interface-util-disclosure-disclosure-97052_>`_

  An interface for managing the visibility of contracts for non\-authorizing parties\.
  
  **viewtype** `V <type-daml-finance-interface-util-disclosure-v-33606_>`_
  
  + **Choice AddObservers**
    
    Add a single new observer context to the existing observers\.
    
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - disclosers
         - :ref:`Parties <type-daml-finance-interface-types-common-parties-68320>`
         - Party calling this choice\.
       * - observersToAdd
         - (`Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_, :ref:`Parties <type-daml-finance-interface-types-common-parties-68320>`)
         - Observer context to add to a contract\.
  
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
  
  + **Choice RemoveObservers**
    
    Remove an observer context from the existing observers\.
    Any party can undisclose itself\. None is returned if no update is needed\.
    
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - disclosers
         - :ref:`Parties <type-daml-finance-interface-types-common-parties-68320>`
         - Party calling this choice\.
       * - observersToRemove
         - (`Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_, :ref:`Parties <type-daml-finance-interface-types-common-parties-68320>`)
         - Observer context to remove\.
  
  + **Choice SetObservers**
    
    Set the observers for a contract\.
    
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - disclosers
         - :ref:`Parties <type-daml-finance-interface-types-common-parties-68320>`
         - Party calling this choice\.
       * - newObservers
         - :ref:`Observers <type-daml-finance-interface-types-common-observers-17879>`
         - Observers to set for this contract\. This overrides the existing observers\.
  
  + **Method archive' \:** `ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Disclosure <type-daml-finance-interface-util-disclosure-disclosure-97052_>`_ \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ ()
    
    Implemetation of archiving the contract\.
  
  + **Method setObservers \:** SetObservers \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Disclosure <type-daml-finance-interface-util-disclosure-disclosure-97052_>`_)
    
    Implementation of the ``SetObservers`` choice\.

Typeclasses
-----------

.. _class-daml-finance-interface-util-disclosure-hasimplementation-29141:

**class** `Implementation <type-daml-finance-interface-util-disclosure-implementation-41553_>`_ t \=\> `HasImplementation <class-daml-finance-interface-util-disclosure-hasimplementation-29141_>`_ t **where**


Data Types
----------

.. _type-daml-finance-interface-util-disclosure-i-26993:

**type** `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  \= `Disclosure <type-daml-finance-interface-util-disclosure-disclosure-97052_>`_
  
  Type synonym for ``Disclosure``\.
  
  **instance** HasMethod :ref:`Account <type-daml-finance-interface-holding-account-account-25212>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Base <type-daml-finance-interface-holding-base-base-14854>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-holding-factory-account-factory-4543>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-holding-factory-holding-factory-29039>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-instrument-base-factory-factory-67517>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Instrument <type-daml-finance-interface-instrument-base-instrument-instrument-22935>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-instrument-bond-fixedrate-factory-27717>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-instrument-bond-floatingrate-factory-71700>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-instrument-bond-inflationlinked-factory-67758>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-instrument-bond-zerocoupon-factory-76014>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-instrument-equity-factory-factory-60517>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Factory <type-daml-finance-interface-instrument-generic-factory-factory-64962>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  **instance** HasMethod :ref:`Instruction <type-daml-finance-interface-settlement-instruction-instruction-30569>` \"asDisclosure\" `I <type-daml-finance-interface-util-disclosure-i-26993_>`_

.. _type-daml-finance-interface-util-disclosure-implementation-41553:

**type** `Implementation <type-daml-finance-interface-util-disclosure-implementation-41553_>`_ t
  \= `HasToInterface <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-interface-hastointerface-68104>`_ t `I <type-daml-finance-interface-util-disclosure-i-26993_>`_
  
  Type constraint for requiring templates to implement ``Disclosure``\.

.. _type-daml-finance-interface-util-disclosure-v-33606:

**type** `V <type-daml-finance-interface-util-disclosure-v-33606_>`_
  \= `View <type-daml-finance-interface-util-disclosure-view-8818_>`_
  
  Type synonym for ``View``\.

.. _type-daml-finance-interface-util-disclosure-view-8818:

**data** `View <type-daml-finance-interface-util-disclosure-view-8818_>`_

  View for ``Disclosure``\.
  
  .. _constr-daml-finance-interface-util-disclosure-view-81921:
  
  `View <constr-daml-finance-interface-util-disclosure-view-81921_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - disclosureControllers
         - `Set <https://docs.daml.com/daml/stdlib/DA-Set.html#type-da-set-types-set-90436>`_ :ref:`Parties <type-daml-finance-interface-types-common-parties-68320>`
         - Disjunction choice controllers\.
       * - observers
         - :ref:`Observers <type-daml-finance-interface-types-common-observers-17879>`
         - Observers with context\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `View <type-daml-finance-interface-util-disclosure-view-8818_>`_
  
  **instance** `Ord <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-ord-6395>`_ `View <type-daml-finance-interface-util-disclosure-view-8818_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `View <type-daml-finance-interface-util-disclosure-view-8818_>`_

Functions
---------

.. _function-daml-finance-interface-util-disclosure-setobservers-55668:

`setObservers <function-daml-finance-interface-util-disclosure-setobservers-55668_>`_
  \: `Disclosure <type-daml-finance-interface-util-disclosure-disclosure-97052_>`_ \-\> SetObservers \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Disclosure <type-daml-finance-interface-util-disclosure-disclosure-97052_>`_)

.. _function-daml-finance-interface-util-disclosure-archivetick-13204:

`archive' <function-daml-finance-interface-util-disclosure-archivetick-13204_>`_
  \: `Disclosure <type-daml-finance-interface-util-disclosure-disclosure-97052_>`_ \-\> `ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Disclosure <type-daml-finance-interface-util-disclosure-disclosure-97052_>`_ \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ ()

.. _function-daml-finance-interface-util-disclosure-flattenobservers-47974:

`flattenObservers <function-daml-finance-interface-util-disclosure-flattenobservers-47974_>`_
  \: :ref:`Observers <type-daml-finance-interface-types-common-observers-17879>` \-\> :ref:`Parties <type-daml-finance-interface-types-common-parties-68320>`
  
  Flattens observers into a ``Set Party`` for usage in template definitions\. For example\:
  
  .. code-block:: daml
  
    observer $ flattenObservers observers
