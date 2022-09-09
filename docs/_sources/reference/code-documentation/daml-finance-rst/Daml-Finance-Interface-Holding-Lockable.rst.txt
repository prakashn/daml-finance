.. Copyright (c) 2022 Digital Asset (Switzerland) GmbH and/or its affiliates. All rights reserved.
.. SPDX-License-Identifier: Apache-2.0

.. _module-daml-finance-interface-holding-lockable-23737:

Module Daml.Finance.Interface.Holding.Lockable
==============================================

Interfaces
----------

.. _type-daml-finance-interface-holding-lockable-lockable-97810:

**interface** `Lockable <type-daml-finance-interface-holding-lockable-lockable-97810_>`_

  An interface respresenting contracts which allow a set of parties to restrict certain actions on a contract\.
  
  **viewtype** `V <type-daml-finance-interface-holding-lockable-v-83344_>`_
  
  + **Choice Acquire**
    
    Lock a contract\.
    
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - newLocker
         - :ref:`Parties <type-daml-finance-interface-types-common-parties-68320>`
         - Parties which restrain the contract's ability to perform specified actions\.
       * - context
         - `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
         - Reason for acquiring a lock\.
       * - lockType
         - `LockType <type-daml-finance-interface-holding-lockable-locktype-36902_>`_
         - Type of lock to acquire
  
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
  
  + **Choice Release**
    
    Unlock a locked contract\.
    
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - context
         - `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
         - 
  
  + **Method acquire \:** Acquire \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Lockable <type-daml-finance-interface-holding-lockable-lockable-97810_>`_)
    
    Implementation of the ``Acquire`` choice\.
  
  + **Method asHolding \:** :ref:`I <type-daml-finance-interface-holding-base-i-67605>`
    
    Conversion to ``Holding`` interface\.
  
  + **Method release \:** Release \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Lockable <type-daml-finance-interface-holding-lockable-lockable-97810_>`_)
    
    Implementation of the ``Release`` choice\.

Typeclasses
-----------

.. _class-daml-finance-interface-holding-lockable-hasimplementation-56813:

**class** `Implementation <type-daml-finance-interface-holding-lockable-implementation-31715_>`_ t \=\> `HasImplementation <class-daml-finance-interface-holding-lockable-hasimplementation-56813_>`_ t **where**


Data Types
----------

.. _type-daml-finance-interface-holding-lockable-i-28871:

**type** `I <type-daml-finance-interface-holding-lockable-i-28871_>`_
  \= `Lockable <type-daml-finance-interface-holding-lockable-lockable-97810_>`_
  
  Type synonym for ``Lockable``\.
  
  **instance** HasMethod :ref:`Transferable <type-daml-finance-interface-holding-transferable-transferable-24986>` \"asLockable\" `I <type-daml-finance-interface-holding-lockable-i-28871_>`_

.. _type-daml-finance-interface-holding-lockable-implementation-31715:

**type** `Implementation <type-daml-finance-interface-holding-lockable-implementation-31715_>`_ t
  \= (`HasToInterface <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-interface-hastointerface-68104>`_ t `I <type-daml-finance-interface-holding-lockable-i-28871_>`_, :ref:`Implementation <type-daml-finance-interface-holding-base-implementation-87781>` t)
  
  Lockable requires Base\.I

.. _type-daml-finance-interface-holding-lockable-lock-96362:

**data** `Lock <type-daml-finance-interface-holding-lockable-lock-96362_>`_

  Locking details\.
  
  .. _constr-daml-finance-interface-holding-lockable-lock-71635:
  
  `Lock <constr-daml-finance-interface-holding-lockable-lock-71635_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - locker
         - :ref:`Parties <type-daml-finance-interface-types-common-parties-68320>`
         - Parties which are locking the contract\.
       * - context
         - `Set <https://docs.daml.com/daml/stdlib/DA-Set.html#type-da-set-types-set-90436>`_ `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
         - Why this lock is held by the locking parties\.
       * - lockType
         - `LockType <type-daml-finance-interface-holding-lockable-locktype-36902_>`_
         - The type of lock applied\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `Lock <type-daml-finance-interface-holding-lockable-lock-96362_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `Lock <type-daml-finance-interface-holding-lockable-lock-96362_>`_

.. _type-daml-finance-interface-holding-lockable-locktype-36902:

**data** `LockType <type-daml-finance-interface-holding-lockable-locktype-36902_>`_

  Type of lock held\.
  
  .. _constr-daml-finance-interface-holding-lockable-semaphore-64839:
  
  `Semaphore <constr-daml-finance-interface-holding-lockable-semaphore-64839_>`_
  
    A one time only lock\.
  
  .. _constr-daml-finance-interface-holding-lockable-reentrant-59422:
  
  `Reentrant <constr-daml-finance-interface-holding-lockable-reentrant-59422_>`_
  
    A mutual exclusion lock where the same lockers may lock a contract multiple times\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `LockType <type-daml-finance-interface-holding-lockable-locktype-36902_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `LockType <type-daml-finance-interface-holding-lockable-locktype-36902_>`_

.. _type-daml-finance-interface-holding-lockable-v-83344:

**type** `V <type-daml-finance-interface-holding-lockable-v-83344_>`_
  \= `View <type-daml-finance-interface-holding-lockable-view-47884_>`_
  
  Type synonym for ``View``\.

.. _type-daml-finance-interface-holding-lockable-view-47884:

**data** `View <type-daml-finance-interface-holding-lockable-view-47884_>`_

  View for ``Lockable``\.
  
  .. _constr-daml-finance-interface-holding-lockable-view-10565:
  
  `View <constr-daml-finance-interface-holding-lockable-view-10565_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - lock
         - `Optional <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-prelude-optional-37153>`_ `Lock <type-daml-finance-interface-holding-lockable-lock-96362_>`_
         - When a contract is locked, contains the locking details\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `View <type-daml-finance-interface-holding-lockable-view-47884_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `View <type-daml-finance-interface-holding-lockable-view-47884_>`_

Functions
---------

.. _function-daml-finance-interface-holding-lockable-asholding-14239:

`asHolding <function-daml-finance-interface-holding-lockable-asholding-14239_>`_
  \: `Lockable <type-daml-finance-interface-holding-lockable-lockable-97810_>`_ \-\> :ref:`I <type-daml-finance-interface-holding-base-i-67605>`

.. _function-daml-finance-interface-holding-lockable-acquire-38088:

`acquire <function-daml-finance-interface-holding-lockable-acquire-38088_>`_
  \: `Lockable <type-daml-finance-interface-holding-lockable-lockable-97810_>`_ \-\> Acquire \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Lockable <type-daml-finance-interface-holding-lockable-lockable-97810_>`_)

.. _function-daml-finance-interface-holding-lockable-release-71:

`release <function-daml-finance-interface-holding-lockable-release-71_>`_
  \: `Lockable <type-daml-finance-interface-holding-lockable-lockable-97810_>`_ \-\> Release \-\> `Update <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-update-68072>`_ (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ `Lockable <type-daml-finance-interface-holding-lockable-lockable-97810_>`_)
