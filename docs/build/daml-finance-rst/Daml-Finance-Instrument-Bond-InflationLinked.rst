.. Copyright (c) 2022 Digital Asset (Switzerland) GmbH and/or its affiliates. All rights reserved.
.. SPDX-License-Identifier: Apache-2.0

.. _module-daml-finance-instrument-bond-inflationlinked-38254:

Module Daml.Finance.Instrument.Bond.InflationLinked
===================================================

Templates
---------

.. _type-daml-finance-instrument-bond-inflationlinked-factory-6079:

**template** `Factory <type-daml-finance-instrument-bond-inflationlinked-factory-6079_>`_

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
    

  + **interface instance** :ref:`Factory <type-daml-finance-interface-instrument-bond-inflationlinked-factory-67758>` **for** `Factory <type-daml-finance-instrument-bond-inflationlinked-factory-6079_>`_
  
  + **interface instance** :ref:`I <type-daml-finance-interface-util-disclosure-i-26993>` **for** `Factory <type-daml-finance-instrument-bond-inflationlinked-factory-6079_>`_

.. _type-daml-finance-instrument-bond-inflationlinked-instrument-89525:

**template** `Instrument <type-daml-finance-instrument-bond-inflationlinked-instrument-89525_>`_

  This template models an inflation linked bond\.
  It pays an inflation adjusted coupon at the end of every coupon period\.
  The coupon is based on a fixed rate, which is applied to a principal that is adjusted according to an inflation index, for example the Consumer Price Index (CPI) in the U\.S\.
  For example\: 0\.5% p\.a\. coupon, CPI adjusted principal\:
  At maturity, the greater of the adjusted principal and the original principal is redeemed\.
  For clarity, this only applies to the redemption amount\. The coupons are always calculated based on the adjusted principal\.
  
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
       - An identifier of the instrument\.
     * - version
       - `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
       - The instrument's version\.
     * - description
       - `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
       - A description of the instrument\.
     * - inflationIndexId
       - `Text <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-text-51952>`_
       - The inflation index reference ID\. For example, in case of \"0\.5% p\.a\. coupon, CPI adjusted principal\" this should be a valid reference to the \"CPI\" index\.
     * - inflationIndexBaseValue
       - `Decimal <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-decimal-18135>`_
       - The value of the inflation index on the first reference date of this bond (called \"dated date\" on US TIPS)\. This is used as the base value for the principal adjustment\.
     * - couponRate
       - `Decimal <https://docs.daml.com/daml/stdlib/Prelude.html#type-ghc-types-decimal-18135>`_
       - The fixed coupon rate, per annum\. For example, in case of a \"0\.5% p\.a\. coupon, CPI adjusted principal\" this should be 0\.005\.
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
       - (Market) time of the last recorded lifecycle event\. If no event has occurred yet, the time of creation should be used\.
  
  + **Choice Archive**
    

  + **interface instance** :ref:`I <type-daml-finance-interface-instrument-base-instrument-i-67236>` **for** `Instrument <type-daml-finance-instrument-bond-inflationlinked-instrument-89525_>`_
  
  + **interface instance** :ref:`I <type-daml-finance-interface-instrument-generic-hasclaims-i-36868>` **for** `Instrument <type-daml-finance-instrument-bond-inflationlinked-instrument-89525_>`_
  
  + **interface instance** :ref:`I <type-daml-finance-interface-lifecycle-rule-lifecycle-i-18685>` **for** `Instrument <type-daml-finance-instrument-bond-inflationlinked-instrument-89525_>`_
  
  + **interface instance** :ref:`I <type-daml-finance-interface-util-disclosure-i-26993>` **for** `Instrument <type-daml-finance-instrument-bond-inflationlinked-instrument-89525_>`_

Data Types
----------

.. _type-daml-finance-instrument-bond-inflationlinked-t-3299:

**type** `T <type-daml-finance-instrument-bond-inflationlinked-t-3299_>`_
  \= `Instrument <type-daml-finance-instrument-bond-inflationlinked-instrument-89525_>`_
  
  Type synonym for ``Instrument``\.
