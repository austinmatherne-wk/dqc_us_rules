# ESEF Data Quality Rules & Guidance

The following automated checks have been drawn from experience with IFRS filings to the SEC and form the initial XBRL International Data Quality Rules in the Beta Release. 

The specification of the current ESEF DQR rules can be found below:

| Number | Short name | Rule version |
| ----- | ----- | ----- |
| [DQC_IFRS_0008](docs/ESEF/DQC_IFRS_0008/DQC_0008.md) | Reversed calculation | 
| [DQC_IFRS_0041](docs/ESEF/DQC_IFRS_0041/DQC_0041.md) | Axis with a default member that differs from the IFRS Taxonomy | 
| [DQC_IFRS_0080](docs/ESEF/DQC_IFRS_0080/DQC_0080.md) | IFRS Non-Negative Items | 
| [DQC_IFRS_0092](docs/ESEF/DQC_IFRS_0092/DQC_0092.md) | IFRS Non-Positive Items | 
| [DQC_IFRS_0093](docs/ESEF/DQC_IFRS_0093/DQC_0093.md) | Durational Aggregation | 
| [DQC_IFRS_0101](docs/ESEF/DQC_IFRS_0101/DQC_0101.md) | Misapplication of Concepts between Investing, Financing and Operating Activities | 
| [DQC_IFRS_0102](docs/ESEF/DQC_IFRS_0102/DQC_0102.md) | Accounting Relationships| 
| [DQC_IFRS_0103](docs/ESEF/DQC_IFRS_0103/DQC_0103.md) | Invalid Value for Percentage Items | 
| [DQC_IFRS_0104](docs/ESEF/DQC_IFRS_0104/DQC_0104.md) | Axis with Inappropriate Members | 
| [DQC_IFRS_0105](docs/ESEF/DQC_IFRS_0105/DQC_0105.md) | FS with No Associated Calculation | 
| [DQC_IFRS_0115](docs/ESEF/DQC_IFRS_0115/DQC_0115.md) | Fact Value Consistency Over Time | 
| [DQC_IFRS_0118](docs/ESEF/DQC_IFRS_0118/DQC_0118.md) | Financial Statement Tables Calculation Check of Required Context | 
| [DQC_IFRS_0126](docs/ESEF/DQC_IFRS_0126/DQC_0126.md) | FS Calculation Check with Non Dimensional Data | 
| [DQC_IFRS_0127](docs/ESEF/DQC_IFRS_0127/DQC_0127.md) | Incorrect Dimensional Item Used on Financial Statements | 
| [DQC_IFRS_0128](docs/ESEF/DQC_IFRS_0128/DQC_0128.md) | Dimensional Values Larger than the Default | 
| [DQC_IFRS_0129](docs/ESEF/DQC_IFRS_0129/DQC_0129.md) | Dimensional Equivalents | 
| [DQC_IFRS_0130](docs/ESEF/DQC_IFRS_0130/DQC_0130.md) | Earnings Per Share Calculation | 
| [DQC_IFRS_0138](docs/ESEF/DQC_IFRS_0138/DQC_0138.md) | Missing Abstract from Financial Statements | 

## Documentation definitions

The rules definitions make reference to the following terms:

* The **extension taxonomy** is the DTS of XBRL Report against which the rules are being evaluated.
* The **base taxonomy** is the IFRS taxonomy corresponding to the ruleset version.  The entry point used for each ruleset is shown below.
* **Monetary** concepts are concepts with a datatype of, or derived from, `xbrli:monetaryItemType`.
* A set of facts are **dimensionally aligned** if they share the same value for all [dimensions](https://www.xbrl.org/Specification/oim/REC-2021-10-13/oim-REC-2021-10-13.html#term-dimension).  Note that this definition refers to the [OIM](https://www.xbrl.org/Specification/oim/REC-2021-10-13/oim-REC-2021-10-13.html) definition of dimension, and so includes the core dimensions such as period and unit, as well as taxonomy-defined dimensions.

## IFRS Entry Points

The following entry points define the _base taxonomy_ for each version of the ruleset:

| Version | Entry point |
| ------- | ----------- | 
| ESEF DQR 2024 | `https://xbrl.ifrs.org/taxonomy/2024-03-27/full_ifrs_entry_point_2024-03-27.xsd` |
| ESEF DQR 2023 | `https://xbrl.ifrs.org/taxonomy/2023-03-23/full_ifrs_entry_point_2023-03-23.xsd` | 
| ESEF DQR 2022 | `http://xbrl.ifrs.org/taxonomy/2022-03-24/full_ifrs_entry_point_2022-03-24.xsd` |  
| ESEF DQR 2021 | `http://xbrl.ifrs.org/taxonomy/2021-03-24/full_ifrs_entry_point_2021-03-24.xsd` |
| ESEF DQR 2020 | `http://xbrl.ifrs.org/taxonomy/2020-03-16/full_ifrs_entry_point_2020-03-16.xsd` |
| ESEF DQR 2019 | `http://xbrl.ifrs.org/taxonomy/2019-03-27/full_ifrs_entry_point_2019-03-27.xsd` |

## Reference implementation

A reference implementation of the ESEF DQR rules is also available.  The reference implementation is defined using the [XULE language](https://xbrl.us/home/use/what-is-xule) developed by XBRL US.  The language is free to use, and an open source [XULE engine](https://github.com/xbrlus/xule/releases/latest) is available for the [Arelle](https://arelle.org/pub) XBRL processor.   


© Copyright 2015 - 2025, XBRL US, Inc. All rights reserved.   
See [License](https://xbrl.us/dqc-license) for license information.  
See [Patent Notice](https://xbrl.us/dqc-patent) for patent infringement notice.  
