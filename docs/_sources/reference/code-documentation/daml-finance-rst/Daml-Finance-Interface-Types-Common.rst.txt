.. Copyright (c) 2022 Digital Asset (Switzerland) GmbH and/or its affiliates. All rights reserved.
.. SPDX-License-Identifier: Apache-2.0

.. _module-daml-finance-interface-types-common-24625:

Module Daml.Finance.Interface.Types.Common
==========================================

Data Types
----------

.. _type-daml-finance-interface-types-common-accountkey-85835:

**data** `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_

  A unique key for Accounts\.
  
  .. _constr-daml-finance-interface-types-common-accountkey-63726:
  
  `AccountKey <constr-daml-finance-interface-types-common-accountkey-63726_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - custodian
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - Party providing accounting services\.
       * - owner
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - Party providing accounting services\.
       * - id
         - `Id <type-daml-finance-interface-types-common-id-56542_>`_
         - Unique identifier for an account\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_
  
  **instance** `Ord <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-ord-6395>`_ `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_
  
  **instance** HasMethod :ref:`Account <type-daml-finance-interface-holding-account-account-25212>` \"getKey\" `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_
  
  **instance** `HasExerciseByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasexercisebykey-36549>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_ GetCid (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`Account <type-daml-finance-interface-holding-account-account-25212>`)
  
  **instance** `HasExerciseByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasexercisebykey-36549>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_ SetCid (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ Reference)
  
  **instance** `HasExerciseByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasexercisebykey-36549>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_ SetObservers (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ Reference)
  
  **instance** `HasExerciseByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasexercisebykey-36549>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_ `Archive <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-template-archive-15178>`_ ()
  
  **instance** `HasFetchByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasfetchbykey-54638>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_
  
  **instance** `HasFromAnyContractKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasfromanycontractkey-95587>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_
  
  **instance** `HasKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-haskey-87616>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_
  
  **instance** `HasLookupByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-haslookupbykey-92299>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_
  
  **instance** `HasMaintainer <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasmaintainer-28932>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_
  
  **instance** `HasToAnyContractKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hastoanycontractkey-35010>`_ Reference `AccountKey <type-daml-finance-interface-types-common-accountkey-85835_>`_

.. _type-daml-finance-interface-types-common-id-56542:

**data** `Id <type-daml-finance-interface-types-common-id-56542_>`_

  .. _constr-daml-finance-interface-types-common-id-52763:
  
  `Id <constr-daml-finance-interface-types-common-id-52763_>`_ `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
  
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `Id <type-daml-finance-interface-types-common-id-56542_>`_
  
  **instance** `Ord <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-ord-6395>`_ `Id <type-daml-finance-interface-types-common-id-56542_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `Id <type-daml-finance-interface-types-common-id-56542_>`_
  
  **instance** `HasExerciseByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasexercisebykey-36549>`_ :ref:`DateClock <type-daml-finance-refdata-time-dateclock-dateclock-68517>` (`Id <type-daml-finance-interface-types-common-id-56542_>`_, `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_) ToNext (`ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`DateClock <type-daml-finance-refdata-time-dateclock-dateclock-68517>`, `ContractId <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-contractid-95282>`_ :ref:`DateClockUpdateEvent <type-daml-finance-refdata-time-dateclock-dateclockupdateevent-11763>`)
  
  **instance** `HasExerciseByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasexercisebykey-36549>`_ :ref:`DateClock <type-daml-finance-refdata-time-dateclock-dateclock-68517>` (`Id <type-daml-finance-interface-types-common-id-56542_>`_, `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_) `Archive <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-template-archive-15178>`_ ()
  
  **instance** `HasExerciseByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasexercisebykey-36549>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_) `Archive <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-template-archive-15178>`_ ()
  
  **instance** `HasFetchByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasfetchbykey-54638>`_ :ref:`DateClock <type-daml-finance-refdata-time-dateclock-dateclock-68517>` (`Id <type-daml-finance-interface-types-common-id-56542_>`_, `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_)
  
  **instance** `HasFetchByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasfetchbykey-54638>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasFromAnyContractKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasfromanycontractkey-95587>`_ :ref:`DateClock <type-daml-finance-refdata-time-dateclock-dateclock-68517>` (`Id <type-daml-finance-interface-types-common-id-56542_>`_, `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_)
  
  **instance** `HasFromAnyContractKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasfromanycontractkey-95587>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-haskey-87616>`_ :ref:`DateClock <type-daml-finance-refdata-time-dateclock-dateclock-68517>` (`Id <type-daml-finance-interface-types-common-id-56542_>`_, `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_)
  
  **instance** `HasKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-haskey-87616>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasLookupByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-haslookupbykey-92299>`_ :ref:`DateClock <type-daml-finance-refdata-time-dateclock-dateclock-68517>` (`Id <type-daml-finance-interface-types-common-id-56542_>`_, `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_)
  
  **instance** `HasLookupByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-haslookupbykey-92299>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasMaintainer <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasmaintainer-28932>`_ :ref:`DateClock <type-daml-finance-refdata-time-dateclock-dateclock-68517>` (`Id <type-daml-finance-interface-types-common-id-56542_>`_, `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_)
  
  **instance** `HasMaintainer <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasmaintainer-28932>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasToAnyContractKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hastoanycontractkey-35010>`_ :ref:`DateClock <type-daml-finance-refdata-time-dateclock-dateclock-68517>` (`Id <type-daml-finance-interface-types-common-id-56542_>`_, `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_)
  
  **instance** `HasToAnyContractKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hastoanycontractkey-35010>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)

.. _type-daml-finance-interface-types-common-instrumentkey-59982:

**data** `InstrumentKey <type-daml-finance-interface-types-common-instrumentkey-59982_>`_

  A unique key for Instruments\.
  
  .. _constr-daml-finance-interface-types-common-instrumentkey-1593:
  
  `InstrumentKey <constr-daml-finance-interface-types-common-instrumentkey-1593_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - depository
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - Party providing depository services\.
       * - issuer
         - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
         - Issuer of instrument\.
       * - id
         - `Id <type-daml-finance-interface-types-common-id-56542_>`_
         - A unique identifier for an instrument\.
       * - version
         - `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
         - A textual instrument version\.
  
  **instance** `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ `InstrumentKey <type-daml-finance-interface-types-common-instrumentkey-59982_>`_
  
  **instance** `Ord <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-ord-6395>`_ `InstrumentKey <type-daml-finance-interface-types-common-instrumentkey-59982_>`_
  
  **instance** `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ `InstrumentKey <type-daml-finance-interface-types-common-instrumentkey-59982_>`_
  
  **instance** HasMethod :ref:`Instrument <type-daml-finance-interface-instrument-base-instrument-instrument-22935>` \"getKey\" `InstrumentKey <type-daml-finance-interface-types-common-instrumentkey-59982_>`_

.. _type-daml-finance-interface-types-common-observers-17879:

**type** `Observers <type-daml-finance-interface-types-common-observers-17879_>`_
  \= `Map <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-map-90052>`_ `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_ (`Set <https://docs.daml.com/daml/stdlib/DA-Set.html#type-da-set-types-set-90436>`_ `Parties <type-daml-finance-interface-types-common-parties-68320_>`_)
  
  Identifies observers of a contract\. The textual key is the \"context\" under which the parties were added as observers\.

.. _type-daml-finance-interface-types-common-parties-68320:

**type** `Parties <type-daml-finance-interface-types-common-parties-68320_>`_
  \= `Set <https://docs.daml.com/daml/stdlib/DA-Set.html#type-da-set-types-set-90436>`_ `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
  
  A set of parties\.
  
  **instance** `HasExerciseByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasexercisebykey-36549>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_) `Archive <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-template-archive-15178>`_ ()
  
  **instance** `HasFetchByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasfetchbykey-54638>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasFromAnyContractKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasfromanycontractkey-95587>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-haskey-87616>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasLookupByKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-haslookupbykey-92299>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasMaintainer <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hasmaintainer-28932>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)
  
  **instance** `HasToAnyContractKey <https://docs.daml.com/daml/stdlib/Prelude.html#class-da-internal-template-functions-hastoanycontractkey-35010>`_ :ref:`Instruction <type-daml-finance-settlement-instruction-instruction-35758>` (`Parties <type-daml-finance-interface-types-common-parties-68320_>`_, `Id <type-daml-finance-interface-types-common-id-56542_>`_)

.. _type-daml-finance-interface-types-common-quantity-79672:

**data** `Quantity <type-daml-finance-interface-types-common-quantity-79672_>`_ u a

  A dimensioned quantity\.
  
  .. _constr-daml-finance-interface-types-common-quantity-77653:
  
  `Quantity <constr-daml-finance-interface-types-common-quantity-77653_>`_
  
    .. list-table::
       :widths: 15 10 30
       :header-rows: 1
    
       * - Field
         - Type
         - Description
       * - unit
         - u
         - The quantity's unit\.
       * - amount
         - a
         - A numerical amount\.
  
  **instance** (`Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ u, `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ a) \=\> `Eq <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-classes-eq-22713>`_ (`Quantity <type-daml-finance-interface-types-common-quantity-79672_>`_ u a)
  
  **instance** (`Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ u, `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ a) \=\> `Show <https://docs.daml.com/daml/stdlib/Prelude.html#class-ghc-show-show-65360>`_ (`Quantity <type-daml-finance-interface-types-common-quantity-79672_>`_ u a)
