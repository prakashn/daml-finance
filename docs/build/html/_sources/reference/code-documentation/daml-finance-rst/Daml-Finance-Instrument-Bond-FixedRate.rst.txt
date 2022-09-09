.. Copyright (c) 2022 Digital Asset (Switzerland) GmbH and/or its affiliates. All rights reserved.
.. SPDX-License-Identifier: Apache-2.0

.. _module-daml-finance-instrument-bond-fixedrate-44039:

Module Daml.Finance.Instrument.Bond.FixedRate
=============================================

Templates
---------

.. _type-daml-finance-instrument-bond-fixedrate-factory-93264:

**template** `Factory <type-daml-finance-instrument-bond-fixedrate-factory-93264_>`_

  Factory template for instrument creation\.
  
  .. list-table::
     :widths: 15 10 30
     :header-rows: 1
  
     * - Field
       - Type
       - Description
     * - provider
       - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
       - The factory's provider\.
     * - observers
       - :ref:`Observers <type-daml-finance-interface-types-common-observers-17879>`
       - The factory's observers\.
  
  + **Choice Archive**
    

  + **interface instance** :ref:`Factory <type-daml-finance-interface-instrument-bond-fixedrate-factory-27717>` **for** `Factory <type-daml-finance-instrument-bond-fixedrate-factory-93264_>`_
  
  + **interface instance** :ref:`I <type-daml-finance-interface-util-disclosure-i-26993>` **for** `Factory <type-daml-finance-instrument-bond-fixedrate-factory-93264_>`_

.. _type-daml-finance-instrument-bond-fixedrate-instrument-788:

**template** `Instrument <type-daml-finance-instrument-bond-fixedrate-instrument-788_>`_

  This template models a fixed rate bond\.
  It pays a fixed coupon rate at the end of every coupon period\.
  
  .. list-table::
     :widths: 15 10 30
     :header-rows: 1
  
     * - Field
       - Type
       - Description
     * - depository
       - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
       - The depository of the instrument\.
     * - issuer
       - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
       - The issuer of the instrument\.
     * - id
       - :ref:`Id <type-daml-finance-interface-types-common-id-56542>`
       - The identifier of the instrument\.
     * - version
       - `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
       - The instrument's version\.
     * - description
       - `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
       - A description of the instrument\.
     * - couponRate
       - `Decimal <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-decimal-18135>`_
       - The fixed coupon rate, per annum\. For example, in case of a \"3\.5% p\.a coupon\" this should be 0\.035\.
     * - periodicSchedule
       - :ref:`PeriodicSchedule <type-daml-finance-interface-types-date-schedule-periodicschedule-97930>`
       - The schedule for the periodic coupon payments\.
     * - holidayCalendarIds
       - \[`Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_\]
       - The identifier of the holiday calendar to be used for the coupon schedule\.
     * - calendarDataProvider
       - `Party <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-party-57932>`_
       - The reference data provider to use for the holiday calendar\.
     * - dayCountConvention
       - :ref:`DayCountConventionEnum <type-daml-finance-interface-types-date-daycount-daycountconventionenum-67281>`
       - The day count convention used to calculate day count fractions\. For example\: Act360\.
     * - currency
       - :ref:`K <type-daml-finance-interface-instrument-base-instrument-k-58546>`
       - The currency of the bond\. For example, if the bond pays in USD this should be a USD cash instrument\.
     * - observers
       - :ref:`Observers <type-daml-finance-interface-types-common-observers-17879>`
       - The observers of the instrument\.
     * - lastEventTimestamp
       - `Time <https://docs.daml.com/daml/stdlib/Prelude.html#type-da-internal-lf-time-63886>`_
       - (Market) time of the last recorded lifecycle event\. If no event has occurred yet, the time of creation should be used\. FIXED\_RATE\_BOND\_TEMPLATE\_END
  
  + **Choice Archive**
    

  + **interface instance** :ref:`I <type-daml-finance-interface-instrument-base-instrument-i-67236>` **for** `Instrument <type-daml-finance-instrument-bond-fixedrate-instrument-788_>`_
  
  + **interface instance** :ref:`I <type-daml-finance-interface-instrument-generic-hasclaims-i-36868>` **for** `Instrument <type-daml-finance-instrument-bond-fixedrate-instrument-788_>`_
  
  + **interface instance** :ref:`I <type-daml-finance-interface-lifecycle-rule-lifecycle-i-18685>` **for** `Instrument <type-daml-finance-instrument-bond-fixedrate-instrument-788_>`_
  
  + **interface instance** :ref:`I <type-daml-finance-interface-util-disclosure-i-26993>` **for** `Instrument <type-daml-finance-instrument-bond-fixedrate-instrument-788_>`_

Data Types
----------

.. _type-daml-finance-instrument-bond-fixedrate-t-14932:

**type** `T <type-daml-finance-instrument-bond-fixedrate-t-14932_>`_
  \= `Instrument <type-daml-finance-instrument-bond-fixedrate-instrument-788_>`_
  
  Type synonym for ``Instrument``\.
