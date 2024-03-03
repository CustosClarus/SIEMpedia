  -----------------------------------------------------------------------
  SIEM USE CASEs configuration and compliance document
  -----------------------------------------------------------------------
  Baselining the systems against SOC operational requirements

  IS Ops team / 14-feb-2013
  -----------------------------------------------------------------------

# Table of Contents {#table-of-contents .TOC-Heading .unnumbered}

[1. Background [8](#background)](#background)

[2. Scope [8](#scope)](#scope)

[3. Responsibility [8](#responsibility)](#responsibility)

[3.1. SOC team [8](#soc-team)](#soc-team)

[3.2. GRC Team [9](#grc-team)](#grc-team)

[3.3. Internal Audit [9](#internal-audit)](#internal-audit)

[3.4. Systems / Control owners
[9](#systems-control-owners)](#systems-control-owners)

[3.5. Management [9](#management)](#management)

[4. Use-Case definition and Attributes
[9](#use-case-definition-and-attributes)](#use-case-definition-and-attributes)

[4.1. Section ID: Network [9](#_Toc349894389)](#_Toc349894389)

[4.1.1. Sub Section ID: Inside Attack
[9](#sub-section-id-inside-attack)](#sub-section-id-inside-attack)

[4.1.1.1. Reference ID: 1.2.1.1.
[9](#reference-id-1.2.1.1.)](#reference-id-1.2.1.1.)

[4.1.1.1.1. Goal [9](#goal)](#goal)

[4.1.1.1.2. Sources [9](#sources)](#sources)

[4.1.1.1.3. Requirements [10](#requirements)](#requirements)

[4.1.1.1.4. Audit to Event-id Mapping
[10](#audit-to-event-id-mapping)](#audit-to-event-id-mapping)

[4.1.1.1.5. Troubleshooting steps
[10](#troubleshooting-steps)](#troubleshooting-steps)

[4.1.1.1.6. Dependency [10](#dependency)](#dependency)

[4.1.1.1.7. Limitations [10](#limitations)](#limitations)

[4.1.1.1.8. Affected Area [10](#affected-area)](#affected-area)

[4.1.1.1.9. References [10](#references)](#references)

[4.1.1.2. Reference ID: 1.2.1.2
[10](#reference-id-1.2.1.2)](#reference-id-1.2.1.2)

[4.1.1.2.1. Goal [10](#goal-1)](#goal-1)

[4.1.1.2.2. Sources [11](#sources-1)](#sources-1)

[4.1.1.2.3. Requirements [11](#requirements-1)](#requirements-1)

[4.1.1.2.4. Audit to Event-id to mapping
[11](#audit-to-event-id-to-mapping)](#audit-to-event-id-to-mapping)

[4.1.1.2.5. Troubleshooting steps
[11](#troubleshooting-steps-1)](#troubleshooting-steps-1)

[4.1.1.2.6. Dependency [11](#dependency-1)](#dependency-1)

[4.1.1.2.7. Limitations [12](#limitations-1)](#limitations-1)

[4.1.1.2.8. Affected Area [12](#affected-area-1)](#affected-area-1)

[4.1.1.2.9. References [12](#references-1)](#references-1)

[4.1.1.3. Reference ID: 1.2.1.3
[12](#reference-id-1.2.1.3)](#reference-id-1.2.1.3)

[4.1.1.3.1. Goal [12](#_Toc349894413)](#_Toc349894413)

[4.1.1.3.2. Sources [12](#sources-2)](#sources-2)

[4.1.1.3.3. Requirements [12](#requirements-2)](#requirements-2)

[4.1.1.3.4. Audit to Event-id to mapping
[12](#audit-to-event-id-to-mapping-1)](#audit-to-event-id-to-mapping-1)

[4.1.1.3.5. Troubleshooting Steps
[12](#troubleshooting-steps-2)](#troubleshooting-steps-2)

[4.1.1.3.6. Dependency [13](#dependency-2)](#dependency-2)

[4.1.1.3.7. Limitations [13](#limitations-2)](#limitations-2)

[4.1.1.3.8. Affected Area [13](#affected-area-2)](#affected-area-2)

[4.1.1.3.9. References [13](#references-2)](#references-2)

[4.1.1.4. Reference ID: 1.2.1.4
[13](#reference-id-1.2.1.4)](#reference-id-1.2.1.4)

[4.1.1.4.1. Goal [13](#goal-3)](#goal-3)

[4.1.1.4.2. Sources [13](#sources-3)](#sources-3)

[4.1.1.4.3. Requirements [13](#requirements-3)](#requirements-3)

[4.1.1.4.4. Audit to Event-id to mapping
[13](#audit-to-event-id-to-mapping-2)](#audit-to-event-id-to-mapping-2)

[4.1.1.4.5. Troubleshooting Steps
[14](#troubleshooting-steps-3)](#troubleshooting-steps-3)

[4.1.1.4.6. Dependency [14](#dependency-3)](#dependency-3)

[4.1.1.4.7. Limitations [14](#limitations-3)](#limitations-3)

[4.1.1.4.8. Affected Area [14](#affected-area-3)](#affected-area-3)

[4.1.1.4.9. References [14](#references-3)](#references-3)

[4.1.1.5. Reference ID: 1.2.1.5
[14](#reference-id-1.2.1.5)](#reference-id-1.2.1.5)

[4.1.1.5.1. Goal [14](#_Toc349894435)](#_Toc349894435)

[4.1.1.5.2. Sources [14](#sources-4)](#sources-4)

[4.1.1.5.3. Requirements [14](#requirements-4)](#requirements-4)

[4.1.1.5.4. Audit to Event-id to mapping
[15](#audit-to-event-id-to-mapping-3)](#audit-to-event-id-to-mapping-3)

[4.1.1.5.5. Troubleshooting Steps
[15](#troubleshooting-steps-4)](#troubleshooting-steps-4)

[4.1.1.5.6. Dependency [15](#dependency-4)](#dependency-4)

[4.1.1.5.7. Limitations [15](#limitations-4)](#limitations-4)

[4.1.1.5.8. Affected Area [15](#affected-area-4)](#affected-area-4)

[4.1.1.5.9. References [15](#references-4)](#references-4)

[4.1.1.6. Reference ID: 1.2.1.6
[15](#reference-id-1.2.1.6)](#reference-id-1.2.1.6)

[4.1.1.6.1. Goal [15](#_Toc349894446)](#_Toc349894446)

[4.1.1.6.2. Sources [15](#sources-5)](#sources-5)

[4.1.1.6.3. Requirements [15](#requirements-5)](#requirements-5)

[4.1.1.6.4. Audit to event-Id mapping
[16](#audit-to-event-id-mapping-1)](#audit-to-event-id-mapping-1)

[4.1.1.6.5. Troubleshooting [16](#troubleshooting)](#troubleshooting)

[4.1.1.6.6. Dependency [16](#dependency-5)](#dependency-5)

[4.1.1.6.7. Limitations [16](#limitations-5)](#limitations-5)

[4.1.1.6.8. Affected Area [16](#affected-area-5)](#affected-area-5)

[4.1.1.6.9. References [16](#references-5)](#references-5)

[4.1.1.7. Reference ID: 1.2.1.7
[16](#reference-id-1.2.1.7)](#reference-id-1.2.1.7)

[4.1.1.7.1. Goal [16](#_Toc349894457)](#_Toc349894457)

[4.1.1.7.2. Sources [16](#sources-6)](#sources-6)

[4.1.1.7.3. Requirements [16](#requirements-6)](#requirements-6)

[4.1.1.7.4. Audit to Event-ID mapping
[17](#audit-to-event-id-mapping-2)](#audit-to-event-id-mapping-2)

[4.1.1.7.5. Troubleshooting steps
[17](#troubleshooting-steps-5)](#troubleshooting-steps-5)

[4.1.1.7.6. Limitations [17](#limitations-6)](#limitations-6)

[4.1.1.7.7. Dependencies [17](#dependencies)](#dependencies)

[4.1.1.7.8. Affected Area [17](#affected-area-6)](#affected-area-6)

[4.1.1.7.9. References [17](#references-6)](#references-6)

[4.1.2. Sub-section ID: External attacks
[17](#sub-section-id-external-attacks)](#sub-section-id-external-attacks)

[4.1.2.1. Reference ID: 1.2.2.1
[17](#reference-id-1.2.2.1)](#reference-id-1.2.2.1)

[4.1.2.1.1. Goal [17](#goal-7)](#goal-7)

[4.1.2.1.2. Sources [17](#sources-7)](#sources-7)

[4.1.2.1.3. Requirements [17](#requirements-7)](#requirements-7)

[4.1.2.1.4. Audit to Event-ID mapping
[17](#audit-to-event-id-mapping-3)](#audit-to-event-id-mapping-3)

[4.1.2.1.5. Troubleshooting steps
[18](#troubleshooting-steps-6)](#troubleshooting-steps-6)

[4.1.2.1.6. Dependency [18](#dependency-6)](#dependency-6)

[4.1.2.1.7. Limitations [19](#limitations-7)](#limitations-7)

[4.1.2.1.8. Affected Area [19](#affected-area-7)](#affected-area-7)

[4.1.2.1.9. References [19](#references-7)](#references-7)

[4.1.2.2. Reference ID: 1.2.2.2
[19](#reference-id-1.2.2.2)](#reference-id-1.2.2.2)

[4.1.2.2.1. Goal [19](#_Toc349894483)](#_Toc349894483)

[4.1.2.2.2. Sources [19](#sources-8)](#sources-8)

[4.1.2.2.3. Requirements [19](#requirements-8)](#requirements-8)

[4.1.2.2.4. Audit to Event-ID mapping
[19](#audit-to-event-id-mapping-4)](#audit-to-event-id-mapping-4)

[4.1.2.2.5. Troubleshooting
[19](#troubleshooting-1)](#troubleshooting-1)

[4.1.2.2.6. Dependency [19](#dependency-7)](#dependency-7)

[4.1.2.2.7. Affected Area [19](#affected-area-8)](#affected-area-8)

[4.1.2.2.8. Limitations [20](#limitations-8)](#limitations-8)

[4.1.2.2.9. References [20](#references-8)](#references-8)

[4.1.2.3. Reference ID: 1.2.2.3
[20](#reference-id-1.2.2.3)](#reference-id-1.2.2.3)

[4.1.2.3.1. Goal [20](#_Toc349894494)](#_Toc349894494)

[4.1.2.3.2. Sources [20](#sources-9)](#sources-9)

[4.1.2.3.3. Requirements [20](#requirements-9)](#requirements-9)

[4.1.2.3.4. Audit to Event-ID mapping
[20](#audit-to-event-id-mapping-5)](#audit-to-event-id-mapping-5)

[4.1.2.3.5. Troubleshooting
[21](#troubleshooting-2)](#troubleshooting-2)

[4.1.2.3.6. Dependency [21](#dependency-8)](#dependency-8)

[4.1.2.3.7. Limitations [21](#limitations-9)](#limitations-9)

[4.1.2.3.8. Affected Area [21](#affected-area-9)](#affected-area-9)

[4.1.2.3.9. References [21](#references-9)](#references-9)

[4.1.2.4. Reference ID: 1.2.2.4
[21](#reference-id-1.2.2.4)](#reference-id-1.2.2.4)

[4.1.2.4.1. Goal [21](#goal-10)](#goal-10)

[4.1.2.4.2. Sources [21](#sources-10)](#sources-10)

[4.1.2.4.3. Requirements [21](#requirements-10)](#requirements-10)

[4.1.2.4.4. Auditing to Event-ID Mapping
[21](#auditing-to-event-id-mapping)](#auditing-to-event-id-mapping)

[4.1.2.4.5. Troubleshooting
[21](#troubleshooting-3)](#troubleshooting-3)

[4.1.2.4.6. Dependency [22](#dependency-9)](#dependency-9)

[4.1.2.4.7. Limitations [22](#limitations-10)](#limitations-10)

[4.1.2.4.8. Affected Area [22](#affected-area-10)](#affected-area-10)

[4.1.2.4.9. References [22](#references-10)](#references-10)

[4.1.2.5. Reference ID: 1.2.2.5
[22](#reference-id-1.2.2.5)](#reference-id-1.2.2.5)

[4.1.2.5.1. Goal [22](#goal-11)](#goal-11)

[4.1.2.5.2. Sources [22](#sources-11)](#sources-11)

[4.1.2.5.3. Requirements [22](#requirements-11)](#requirements-11)

[4.1.2.5.4. Auditing to Event-ID Mapping
[22](#auditing-to-event-id-mapping-1)](#auditing-to-event-id-mapping-1)

[4.1.2.5.5. Troubleshooting steps
[23](#troubleshooting-steps-7)](#troubleshooting-steps-7)

[4.1.2.5.6. Dependency [23](#dependency-10)](#dependency-10)

[4.1.2.5.7. Limitations [23](#limitations-11)](#limitations-11)

[4.1.2.5.8. Affected Area [23](#affected-area-11)](#affected-area-11)

[4.1.2.5.9. References [23](#references-11)](#references-11)

[4.1.3. Sub-section ID: Visibility
[23](#sub-section-id-visibility)](#sub-section-id-visibility)

[4.1.3.1. Reference ID: 1.2.3.1
[23](#reference-id-1.2.3.1)](#reference-id-1.2.3.1)

[4.1.3.1.1. Goal [23](#goal-12)](#goal-12)

[4.1.3.1.2. Sources [24](#sources-12)](#sources-12)

[4.1.3.1.3. Requirements [24](#requirements-12)](#requirements-12)

[4.1.3.1.4. Auditing to Event-ID Mapping
[24](#auditing-to-event-id-mapping-2)](#auditing-to-event-id-mapping-2)

[4.1.3.1.5. Troubleshooting
[24](#troubleshooting-4)](#troubleshooting-4)

[4.1.3.1.6. Dependency [24](#dependency-11)](#dependency-11)

[4.1.3.1.7. Limitations [25](#limitations-12)](#limitations-12)

[4.1.3.1.8. Affected Area [25](#affected-area-12)](#affected-area-12)

[4.1.3.1.9. References [25](#references-12)](#references-12)

[4.1.3.2. Reference ID: 1.2.3.2
[25](#reference-id-1.2.3.2)](#reference-id-1.2.3.2)

[4.1.3.2.1. Goal [25](#goal-13)](#goal-13)

[4.1.3.2.2. Sources [25](#sources-13)](#sources-13)

[4.1.3.2.3. Requirements [25](#requirements-13)](#requirements-13)

[4.1.3.2.4. Auditing to Event-ID Mapping
[26](#auditing-to-event-id-mapping-3)](#auditing-to-event-id-mapping-3)

[4.1.3.2.5. Troubleshooting
[26](#troubleshooting-5)](#troubleshooting-5)

[4.1.3.2.6. Dependency [26](#dependency-12)](#dependency-12)

[4.1.3.2.7. Limitations [26](#limitations-13)](#limitations-13)

[4.1.3.2.8. Affected Area [26](#affected-area-13)](#affected-area-13)

[4.1.3.2.9. References [26](#references-13)](#references-13)

[4.1.3.3. Reference ID: 1.2.3.3
[26](#reference-id-1.2.3.3)](#reference-id-1.2.3.3)

[4.1.3.3.1. Goal [26](#goal-14)](#goal-14)

[4.1.3.3.2. Sources [27](#sources-14)](#sources-14)

[4.1.3.3.3. Requirements [27](#requirements-14)](#requirements-14)

[4.1.3.3.4. Auditing to Event-ID Mapping
[27](#auditing-to-event-id-mapping-4)](#auditing-to-event-id-mapping-4)

[4.1.3.3.5. Troubleshooting
[27](#troubleshooting-6)](#troubleshooting-6)

[4.1.3.3.6. Dependency [27](#dependency-13)](#dependency-13)

[4.1.3.3.7. Limitations [28](#limitations-14)](#limitations-14)

[4.1.3.3.8. Affected Area [28](#affected-area-14)](#affected-area-14)

[4.1.3.3.9. References [28](#references-14)](#references-14)

[4.1.3.4. Reference ID: 1.2.3.4
[28](#reference-id-1.2.3.4)](#reference-id-1.2.3.4)

[4.1.3.4.1. Goal [28](#goal-15)](#goal-15)

[4.1.3.4.2. Sources [28](#sources-15)](#sources-15)

[4.1.3.4.3. Requirements [28](#requirements-15)](#requirements-15)

[4.1.3.4.4. Auditing to Event-ID Mapping
[28](#auditing-to-event-id-mapping-5)](#auditing-to-event-id-mapping-5)

[4.1.3.4.5. Troubleshooting
[29](#troubleshooting-7)](#troubleshooting-7)

[4.1.3.4.6. Dependency [29](#dependency-14)](#dependency-14)

[4.1.3.4.7. Limitations [29](#limitations-15)](#limitations-15)

[4.1.3.4.8. Affected Area [29](#affected-area-15)](#affected-area-15)

[4.1.3.4.9. References [29](#references-15)](#references-15)

[4.1.3.5. Reference ID: 1.2.3.5
[29](#reference-id-1.2.3.5)](#reference-id-1.2.3.5)

[4.1.3.5.1. Goal [29](#goal-16)](#goal-16)

[4.1.3.5.2. Sources [29](#sources-16)](#sources-16)

[4.1.3.5.3. Requirements [30](#requirements-16)](#requirements-16)

[4.1.3.5.4. Auditing to Event-ID Mapping
[30](#auditing-to-event-id-mapping-6)](#auditing-to-event-id-mapping-6)

[4.1.3.5.5. Troubleshooting
[30](#troubleshooting-8)](#troubleshooting-8)

[4.1.3.5.6. Dependency [30](#dependency-15)](#dependency-15)

[4.1.3.5.7. Affected Area [30](#affected-area-16)](#affected-area-16)

[4.1.3.5.8. Limitations [30](#limitations-16)](#limitations-16)

[4.1.3.5.9. References [31](#references-16)](#references-16)

[4.1.3.6. Reference ID: 1.2.3.6
[31](#reference-id-1.2.3.6)](#reference-id-1.2.3.6)

[4.1.3.6.1. Goal [31](#goal-17)](#goal-17)

[4.1.3.6.2. Sources [31](#sources-17)](#sources-17)

[4.1.3.6.3. Requirements [31](#requirements-17)](#requirements-17)

[4.1.3.6.4. Auditing to Event-ID Mapping
[31](#auditing-to-event-id-mapping-7)](#auditing-to-event-id-mapping-7)

[4.1.3.6.5. Troubleshooting
[32](#troubleshooting-9)](#troubleshooting-9)

[4.1.3.6.6. Dependency [32](#dependency-16)](#dependency-16)

[4.1.3.6.7. Limitations [32](#limitations-17)](#limitations-17)

[4.1.3.6.8. Affected Area [32](#affected-area-17)](#affected-area-17)

[4.1.3.6.9. References [32](#references-17)](#references-17)

[4.1.3.7. Reference ID: 1.2.3.7
[32](#reference-id-1.2.3.7)](#reference-id-1.2.3.7)

[4.1.3.7.1. Goal [32](#goal-18)](#goal-18)

[4.1.3.7.2. Sources [32](#sources-18)](#sources-18)

[4.1.3.7.3. Requirements [32](#requirements-18)](#requirements-18)

[4.1.3.7.4. Auditing to Event-ID Mapping
[33](#auditing-to-event-id-mapping-8)](#auditing-to-event-id-mapping-8)

[4.1.3.7.5. Troubleshooting
[33](#troubleshooting-10)](#troubleshooting-10)

[4.1.3.7.6. Dependency [33](#dependency-17)](#dependency-17)

[4.1.3.7.7. Limitations [33](#limitations-18)](#limitations-18)

[4.1.3.7.8. Affected Area [33](#affected-area-18)](#affected-area-18)

[4.1.3.7.9. References [33](#references-18)](#references-18)

[4.1.3.8. Reference ID: 1.2.3.8
[33](#reference-id-1.2.3.8)](#reference-id-1.2.3.8)

[4.1.3.8.1. Goal [33](#goal-19)](#goal-19)

[4.1.3.8.2. Sources [33](#sources-19)](#sources-19)

[4.1.3.8.3. Requirements [34](#requirements-19)](#requirements-19)

[4.1.3.8.4. Auditing to Event-ID Mapping
[34](#auditing-to-event-id-mapping-9)](#auditing-to-event-id-mapping-9)

[4.1.3.8.5. Troubleshooting
[34](#troubleshooting-11)](#troubleshooting-11)

[4.1.3.8.6. Dependency [34](#dependency-18)](#dependency-18)

[4.1.3.8.7. Limitations [34](#limitations-19)](#limitations-19)

[4.1.3.8.8. Affected Area [35](#affected-area-19)](#affected-area-19)

[4.1.3.8.9. References [35](#references-19)](#references-19)

[4.1.3.9. Reference ID: 1.2.3.9
[35](#reference-id-1.2.3.9)](#reference-id-1.2.3.9)

[4.1.3.9.1. Goal [35](#goal-20)](#goal-20)

[4.1.3.9.2. Sources [35](#sources-20)](#sources-20)

[4.1.3.9.3. Requirements [35](#requirements-20)](#requirements-20)

[4.1.3.9.4. Auditing to Event-ID Mapping
[36](#auditing-to-event-id-mapping-10)](#auditing-to-event-id-mapping-10)

[4.1.3.9.5. Troubleshooting
[36](#troubleshooting-12)](#troubleshooting-12)

[4.1.3.9.6. Dependency [36](#dependency-19)](#dependency-19)

[4.1.3.9.7. Limitations [36](#limitations-20)](#limitations-20)

[4.1.3.9.8. Affected Area [36](#affected-area-20)](#affected-area-20)

[4.1.3.9.9. References [36](#references-20)](#references-20)

[4.1.3.10. Reference ID: 1.2.3.10
[37](#reference-id-1.2.3.10)](#reference-id-1.2.3.10)

[4.1.3.10.1. Goal [37](#goal-21)](#goal-21)

[4.1.3.10.2. Sources [37](#sources-21)](#sources-21)

[4.1.3.10.3. Requirements [37](#requirements-21)](#requirements-21)

[4.1.3.10.4. Auditing to Event-ID Mapping
[37](#auditing-to-event-id-mapping-11)](#auditing-to-event-id-mapping-11)

[4.1.3.10.5. Troubleshooting
[37](#troubleshooting-13)](#troubleshooting-13)

[4.1.3.10.6. Dependency [38](#dependency-20)](#dependency-20)

[4.1.3.10.7. Limitations [38](#limitations-21)](#limitations-21)

[4.1.3.10.8. Affected Area [38](#affected-area-21)](#affected-area-21)

[4.1.3.10.9. References [38](#references-21)](#references-21)

[4.1.3.11. Reference ID: 1.2.3.11
[38](#reference-id-1.2.3.11)](#reference-id-1.2.3.11)

[4.1.3.11.1. Goal [38](#goal-22)](#goal-22)

[4.1.3.11.2. Sources [38](#sources-22)](#sources-22)

[4.1.3.11.3. Requirements [38](#requirements-22)](#requirements-22)

[4.1.3.11.4. Auditing to Event-ID Mapping
[39](#auditing-to-event-id-mapping-12)](#auditing-to-event-id-mapping-12)

[4.1.3.11.5. Troubleshooting
[39](#troubleshooting-14)](#troubleshooting-14)

[4.1.3.11.6. Dependency [39](#dependency-21)](#dependency-21)

[4.1.3.11.7. Limitations [39](#limitations-22)](#limitations-22)

[4.1.3.11.8. Affected Area [39](#affected-area-22)](#affected-area-22)

[4.1.3.11.9. References [39](#references-22)](#references-22)

[4.1.4. Sub-section ID: Policy violations
[40](#sub-section-id-policy-violations)](#sub-section-id-policy-violations)

[4.1.4.1. Reference ID: 1.2.4.1
[40](#reference-id-1.2.4.1)](#reference-id-1.2.4.1)

[4.1.4.1.1. Goal [40](#goal-23)](#goal-23)

[4.1.4.1.2. Sources [40](#sources-23)](#sources-23)

[4.1.4.1.3. Requirements [40](#requirements-23)](#requirements-23)

[4.1.4.1.4. Auditing to Event-ID Mapping
[40](#auditing-to-event-id-mapping-13)](#auditing-to-event-id-mapping-13)

[4.1.4.1.5. Troubleshooting
[40](#troubleshooting-15)](#troubleshooting-15)

[4.1.4.1.6. Dependency [40](#dependency-22)](#dependency-22)

[4.1.4.1.7. Limitations [41](#limitations-23)](#limitations-23)

[4.1.4.1.8. Affected Area [41](#affected-area-23)](#affected-area-23)

[4.1.4.1.9. References [41](#references-23)](#references-23)

[4.1.4.2. Reference ID: 1.2.4.2
[41](#reference-id-1.2.4.2)](#reference-id-1.2.4.2)

[4.1.4.2.1. Goal [41](#goal-24)](#goal-24)

[4.1.4.2.2. Sources [41](#sources-24)](#sources-24)

[4.1.4.2.3. Requirements [41](#requirements-24)](#requirements-24)

[4.1.4.2.4. Auditing to Event-ID Mapping
[41](#auditing-to-event-id-mapping-14)](#auditing-to-event-id-mapping-14)

[4.1.4.2.5. Troubleshooting
[42](#troubleshooting-16)](#troubleshooting-16)

[4.1.4.2.6. Dependency [42](#dependency-23)](#dependency-23)

[4.1.4.2.7. Limitations [42](#limitations-24)](#limitations-24)

[4.1.4.2.8. Affected Area [42](#affected-area-24)](#affected-area-24)

[4.1.4.2.9. References [42](#references-24)](#references-24)

[4.1.5. Sub-section ID: Operations
[42](#sub-section-id-operations)](#sub-section-id-operations)

[4.1.5.1. Reference ID: 1.2.5.1
[42](#reference-id-1.2.5.1)](#reference-id-1.2.5.1)

[4.1.5.1.1. Goal [42](#goal-25)](#goal-25)

[4.1.5.1.2. Sources [42](#sources-25)](#sources-25)

[4.1.5.1.3. Requirements [42](#requirements-25)](#requirements-25)

[4.1.5.1.4. Auditing to Event-ID Mapping
[43](#auditing-to-event-id-mapping-15)](#auditing-to-event-id-mapping-15)

[4.1.5.1.5. Troubleshooting
[43](#troubleshooting-17)](#troubleshooting-17)

[4.1.5.1.6. Dependency [43](#dependency-24)](#dependency-24)

[4.1.5.1.7. Limitations [43](#limitations-25)](#limitations-25)

[4.1.5.1.8. Affected Area [43](#affected-area-25)](#affected-area-25)

[4.1.5.1.9. References [43](#references-25)](#references-25)

[4.1.6. Sub-section ID: Legal
[44](#sub-section-id-legal)](#sub-section-id-legal)

[4.1.6.1. Reference ID: 1.2.6.1
[44](#reference-id-1.2.6.1)](#reference-id-1.2.6.1)

[4.1.6.1.1. Goal [44](#goal-26)](#goal-26)

[4.1.6.1.2. Sources [44](#sources-26)](#sources-26)

[4.1.6.1.3. Requirements [44](#requirements-26)](#requirements-26)

[4.1.6.1.4. Auditing to Event-ID Mapping
[44](#auditing-to-event-id-mapping-16)](#auditing-to-event-id-mapping-16)

[4.1.6.1.5. Troubleshooting
[45](#troubleshooting-18)](#troubleshooting-18)

[4.1.6.1.6. Dependency [45](#dependency-25)](#dependency-25)

[4.1.6.1.7. Limitations [45](#limitations-26)](#limitations-26)

[4.1.6.1.8. Affected Area [45](#affected-area-26)](#affected-area-26)

[4.1.6.1.9. References [45](#references-26)](#references-26)

**[Document Information]{.underline}**

  -----------------------------------------------------------------------
  **Document Title**   **Incident Response Policy**
  -------------------- --------------------------------------------------
  **Drafted by**       NADRA IS Operations team

  **Draft Date**       Jan 5, 2013

  **Owner**            NADRA

  **Classification/    Internal / NADRA
  Classification       
  Authority**          

  **Release Version**  1.1

  **Reference          SOC implementation plan
  document**           

  **Approval Date**    

  **Approved By**      

  **Published Date**   
  -----------------------------------------------------------------------

# Background

> The purpose of this document is to illustrate assets owners the
> underlying procedural requirements and configurations necessary to
> operate and sustain SOC operations. The understanding of these
> requirements by owners is critically important in determining the
> success of SOC operations, In case of any change resulting due to
> improper configuration or management of these requirements can
> directly impact the performance of SOC operations team in timely
> detection and response to security incidents.

# Scope

The scope of this exercise stretches within the bounds of use-cases
requirements mentioned in the SOC implementation plan referenced above
(Document Information).

# Responsibility

######### SOC team 

The team is responsible for:-

-   Maintaining an auditable trail to prove events of interest were
    followed up on and resolved.

-   Active monitoring of controls

#########  GRC Team

> The team is responsible to update, maintain policies for relevancy and
> to reflect the configuration requirements herein mentioned.

#########  Internal Audit 

> The audit is responsible for:-

-   Reviewing the internal controls, periodically or as mentioned in
    annual audit plan or as directed by the regulator, implemented by
    senior management.

-   Internal auditors will evaluate and review the internal controls in
    place and report for its improvements.

-   To ensure that SOPs are followed by concerned department and grey
    areas, if any, are identified with recommendations how to counter
    the same.

#########  Systems / Control owners 

> The owners are responsible for:-

-   Introducing internal Controls through SOPs which are prepared in
    consultation with respective departmental heads, reviewed and
    approved by management for implementing the same.

-   Configuration and management of audit rules as per policies (e.g
    Change and configuration management policy).

#########  Management

> The management is responsible for:-

-   Establishing a mechanism to update the audit procedures.

-   Establishing a periodic review of audit activities and to adjust
    those audit activities to better support the NADRA's business goals.

# Use-Case definition and Attributes

1.  

######### Section ID: Network

### Sub Section ID: Inside Attack

#### Reference ID: 1.2.1.1.

##### Goal

Under this use-case the SOC operations team would be detecting a new VPN
connection

##### Sources

> Aggregate firewall

##### Requirements

a.  Enable syslog on cisco asa 5825. \[1\]

###################################################  {#section .unnumbered}

b.  Filtering syslog messages for VPN session establishment.

##### Audit to Event-id Mapping

> N/A

##### Troubleshooting steps

> N/A

#####  Dependency 

> N/A

##### Limitations

> N/A

##### Affected Area

-   All NADRA VPN aggregation firewalls.

##### References 

> \[1\]http://www.cisco.com/en/US/docs/security/asa/asa84/configuration/guide/monitor_syslog.html#wp1552182
>
> \[2\]
> <http://www.confighelper.com/2009/07/how-to-check-cisco-asa-vpn-activity-using-syslog.html>

#### Reference ID: 1.2.1.2

##### Goal

Under this use-case the SOC operations team would be monitoring events
for MAC flooding attack

##### Sources

> AIP module firewall

##### Requirements 

a.  Enable syslog on same as reference id: 1.2.1.1

b.  Filtering syslog messages for MAC flooding attempts. \[1\]

##### Audit to Event-id to mapping 

  -----------------------------------------------------------------------------
  Details 1         
  ----------------- -----------------------------------------------------------
  **Product:**      AIP module

  **Maps to**       4.1.1.2.3

  **Event ID:**     322001

  **Description**   The adaptive security appliance received a packet from the
                    offending MAC address on the specified interface, but the
                    source MAC address in the packet is statically bound to
                    another interface in the configuration. Either a
                    MAC-spoofing attack or a misconfiguration may be the cause.
  -----------------------------------------------------------------------------

  -----------------------------------------------------------------------------
  Details 2         
  ----------------- -----------------------------------------------------------
  **Product:**      AIP module

  **Maps to**       4.1.1.2.3

  **Event ID:**     322002

  **Description**   If the ARP inspection module is enabled, it checks whether
                    a new ARP entry advertised in the packet conforms to the
                    statically configured or dynamically learned IP-MAC address
                    binding before forwarding ARP packets across the adaptive
                    security appliance. If this check fails, the ARP inspection
                    module drops the ARP packet and generates this message.
                    This situation may be caused by either ARP spoofing attacks
                    in the network or an invalid configuration (IP-MAC
                    binding).
  -----------------------------------------------------------------------------

##### Troubleshooting steps

> N/A

##### Dependency

> N/A

##### Limitations

> N/A

##### Affected Area

-   All NADRA vlans.

##### References 

> \[1\]<http://www.cisco.com/en/US/docs/security/asa/asa83/system/message/logmsgs.html>

#### Reference ID: 1.2.1.3 

1.  

##### Goal

> Under this use-case the SOC operations team would be monitoring events
> for scanning attempt made by intruder / attacker

##### Sources 

> AIP module

##### Requirements

a.  Enable syslog on same as reference id: 1.2.1.1

b.  Filtering syslog messages for scanning. \[1\]

##### Audit to Event-id to mapping 

  -----------------------------------------------------------------------------
  Details 1         
  ----------------- -----------------------------------------------------------
  **Product:**      AIP module

  **Maps to**       4.1.1.2.3

  **Event ID:**     733101

  **Description**   The adaptive security appliance detected that a specific
                    host (or several hosts in the same 1024-node subnet) is
                    either scanning the network (attacking), or is being
                    scanned (targeted)
  -----------------------------------------------------------------------------

##### Troubleshooting Steps

> N/A

##### Dependency 

N/A

##### Limitations 

> N/A

##### Affected Area

> Against Windows critical servers
>
> Against unix critical servers
>
> Against critical network devices

##### References

> \[1\]http://www.cisco.com/en/US/docs/security/asa/asa83/system/message/logmsgs.html#wp4771499

####  Reference ID: 1.2.1.4

1.  

#####  Goal

> Under this use-case the SOC operations team would be monitoring events
> for DHCP starvation attack

##### Sources

> Nexsus 7018, Juniper IDP

##### Requirements

a.  Configure Nexsus to enable DHCP snooping feature to prevent rogue
    DHCP and starvation attacks

b.  Configure syslog protocol to send DHCP snooping events.\[1\]

##### Audit to Event-id to mapping 

> N/A

##### Troubleshooting Steps

> N/A

##### Dependency 

> N/A

##### Limitations 

1.  The SOC team relies on properly configured and secure NEXSUS switch
    to enable necessary protection (e.g DHCP snooping).

##### Affected Area

> NADRA Active directory.

##### References 

> \[1\]http://www.cisco.com/en/US/docs/solutions/Enterprise/Security/SAFE_RG/chap8.html#wp1060946

#### Reference ID: 1.2.1.5

1.  

##### Goal

> Under this use-case the SOC operations team would be monitoring rogue
> AP\'s.

##### Sources

> CISCO MSE

##### Requirements 

1.  Configure Remote Syslog Server to publish MSE logs \[1\]

```{=html}
<!-- -->
```
a.  Use this option to configure a Remote Syslog Server by specifying
    the IP address, priority parameter, priority level, and facility.

b.  A Remote Syslog Server has not been configured for this machine.

c.  Configure Remote Syslog Server Configuration parameters?
    (Y)es/(S)kip/(U)se default

d.  \[Skip\]: y

e.  Configure Remote Syslog Server IP address

f.  Configure Remote Syslog Server Priority parameter.

g.  select a priority level

h.  Configure Remote Syslog Server\'s Facility parameter.

i.  Select a logging facility

##### Audit to Event-id to mapping 

> N/A

##### Troubleshooting Steps

> N/A

##### Dependency 

> N/A

##### Limitations 

> N/A

##### Affected Area

> All NADRA wifi-users / SSIDs

##### References

> \[1\]http://www.cisco.com/en/US/docs/wireless/mse/3350/7.0MR1/CAS/configuration/guide/msecg71_appA_Hardening.html#wp1275151

#### Reference ID: 1.2.1.6

1.  

##### Goal

> Under this use-case the SOC operations team would be monitoring when a
> new VPN site has been cause of worm propagation to other networks.

##### Sources

> CISCO IDP logs, Symantec End-point

##### Requirements

a.  **Enabling steps**

```{=html}
<!-- -->
```
1.  Configure the CISCO ASA firewall IDP module to send syslog to Q1
    radar appliance.

2.  Configure the Symantec end-point server to do the same.

##### Audit to event-Id mapping

> N/A

##### Troubleshooting

> N/A

##### Dependency 

> Reference number 1.1.2.1 & Reference number 1.2.1.1

##### Limitations 

> N/A

##### Affected Area

> ALL NADRA Vlans.

##### References

> N/A

#### Reference ID: 1.2.1.7

1.  

##### Goal

> Under this use-case the SOC operations team would be monitoring If X
> number of attempts have seen accessing FTP server using default
> credentials.

##### Sources 

> CISCO IDP logs

##### Requirements

a.  **Enabling steps**

```{=html}
<!-- -->
```
1.  Configure the CISCO IDP to send brute-force event messages via
    syslog.

2.  Configuring OSSEC agent to alert on ftp brute force attempts. \[1\]

##### Audit to Event-ID mapping 

> N/A

##### **Troubleshooting steps**

> N/A

##### **Limitations**

> Access to Nessus server is unavailable.

##### **Dependencies** 

> N/A

##### Affected Area

> FTP server farm

##### **References** 

> \[1\]www.ossec.net/doc/rules/rules/50_ms_ftpd_rules.xml.html+&cd=1&hl=en&ct=clnk&gl=pk&client=firefox-a

### Sub-section ID: External attacks

#### Reference ID: 1.2.2.1

4.  

    2.  

    3.  1.  

#####  Goal

> Under this use-case the SOC operations team would be monitoring for
> fragmented ICMP traffic entering or leaving the network.

##### Sources

> CISCO IDP logs

##### Requirements

1.  Configure the CISCO IDP to send fragmented traffic event messages
    via syslog.

##### Audit to Event-ID mapping 

  -----------------------------------------------------------------------------
  Details 1 \[1\]   
  ----------------- -----------------------------------------------------------
  **Product:**      AIP module

  **Maps to**       4.1.1.2.3

  **Signature ID**  1100

  **Message         400007
  Number**          

  **Signature       IP Fragment Attack
  Title**           

  **Signature       Attack
  Type**            

  **Description**   Triggers when any IP datagram is received with an offset
                    value less than 5 but greater than 0 indicated in the
                    offset field.
  -----------------------------------------------------------------------------

  -----------------------------------------------------------------------------
  Details 2         
  ----------------- -----------------------------------------------------------
  **Product:**      AIP module

  **Maps to**       4.1.1.2.3

  **Signature ID**  1100

  **Message         400009
  Number**          

  **Signature       IP Overlapping Fragments (Teardrop)
  Title**           

  **Signature       Attack
  Type**            

  **Description**   Triggers when two fragments contained within the same IP
                    datagram have offsets that indicate that they share
                    positioning within the datagram. This could mean that
                    fragment A is being completely overwritten by fragment B,
                    or that fragment A is partially being overwritten by
                    fragment B. Some operating systems do not properly handle
                    fragments that overlap in this manner and may throw
                    exceptions or behave in other undesirable ways upon receipt
                    of overlapping fragments, which is how the Teardrop attack
                    works to create a DoS.
  -----------------------------------------------------------------------------

##### Troubleshooting steps

> N/A

##### Dependency 

> N/A

##### Limitations

> N/A

##### Affected Area

> All Vlans

##### References 

> \[1\]http://www.cisco.com/en/US/docs/security/asa/asa84/configuration/guide/protect_tools.html

#### Reference ID: 1.2.2.2

1.  

##### Goal

> Under this use-case the SOC operations team would be monitoring for
> ping sweep events.

##### Sources

> CISCO ASA 5585

##### Requirements

1.  Configure the CISCO IDP to send ping sweep event messages via
    > syslog.

##### Audit to Event-ID mapping 

> N/A

##### Troubleshooting 

> N/A

##### Dependency 

> N/A

##### Affected Area

> All Vlans

##### Limitations 

1.  Syslog traffic is being blocked or filtered by network and proxies.

2.  The recent patch has broken down the functionality of the syslog
    > agent.

3.  If the admin exclude his / her account from auditing.

##### References 

> \[1\]http://www.cisco.com/en/US/docs/security/asa/asa84/system/message/logmsgs.html#wp4769400

#### Reference ID: 1.2.2.3 

4.  

##### Goal

> Under this use-case the SOC operations team would be monitoring for
> operating system fingerprinting event.

##### Sources

> CISCO IDP logs

##### Requirements

1.  Configure the CISCO IDP to send events logs related to signature
    mentioned in section 4.1.2.3.4

##### Audit to Event-ID mapping 

+---------+---+---+--------+-----------------------------------------------+
| Details |   |   |        |                                               |
| 1 \[1\] |   |   |        |                                               |
+=========+===+===+========+===============================================+
| **Pro   | A |   |        |                                               |
| duct:** | I |   |        |                                               |
|         | P |   |        |                                               |
|         | m |   |        |                                               |
|         | o |   |        |                                               |
|         | d |   |        |                                               |
|         | u |   |        |                                               |
|         | l |   |        |                                               |
|         | e |   |        |                                               |
+---------+---+---+--------+-----------------------------------------------+
| **Maps  | 4 |   |        |                                               |
| to**    | . |   |        |                                               |
|         | 1 |   |        |                                               |
|         | . |   |        |                                               |
|         | 2 |   |        |                                               |
|         | . |   |        |                                               |
|         | 3 |   |        |                                               |
+---------+---+---+--------+-----------------------------------------------+
| Si      |   | S |        | Comments                                      |
| gnature |   | i |        |                                               |
| ID      |   | g |        |                                               |
|         |   | n |        |                                               |
|         |   | a |        |                                               |
|         |   | t |        |                                               |
|         |   | u |        |                                               |
|         |   | r |        |                                               |
|         |   | e |        |                                               |
|         |   | P |        |                                               |
|         |   | a |        |                                               |
|         |   | c |        |                                               |
|         |   | k |        |                                               |
+---------+---+---+--------+-----------------------------------------------+
| 3046/0  |   |   |        | This signature looks for a unique combination |
|         |   |   |        | of TCP packets that the NMAP tool uses to     |
|         |   | - |        | fingerprint a remote operating system.        |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   |   |        |                                               |
|         |   |   |        |                                               |
|         |   |   |        |                                               |
|         |   |   |        |                                               |
|         |   |   |        |                                               |
|         |   | S |        |                                               |
|         |   | 3 |        |                                               |
|         |   |   |        |                                               |
|         |   |   |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   |   |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   |   |        |                                               |
|         |   |   |        |                                               |
|         |   |   |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
|         |   | - |        |                                               |
+---------+---+---+--------+-----------------------------------------------+
| **Si    |   | O |        |                                               |
| gnature |   | S |        |                                               |
| Title** |   | f |        |                                               |
|         |   | i |        |                                               |
|         |   | n |        |                                               |
|         |   | g |        |                                               |
|         |   | e |        |                                               |
|         |   | r |        |                                               |
|         |   | p |        |                                               |
|         |   | r |        |                                               |
|         |   | i |        |                                               |
|         |   | n |        |                                               |
|         |   | t |        |                                               |
|         |   | i |        |                                               |
|         |   | n |        |                                               |
|         |   | g |        |                                               |
+---------+---+---+--------+-----------------------------------------------+
| **Si    |   |   | Attack |                                               |
| gnature |   |   |        |                                               |
| Type**  |   |   |        |                                               |
+---------+---+---+--------+-----------------------------------------------+

##### Troubleshooting

> N/A

##### Dependency 

> N/A

##### Limitations 

1.  Syslog traffic is being blocked or filtered by network and proxies.

2.  The recent patch has broken down the functionality of the syslog
    agent.

3.  If the admin exclude his / her account from auditing.

##### Affected Area

> Unix and windows critical servers

##### References 

> \[1\]http://www.cisco.com/en/US/docs/security/asa/asa84/system/message/logmsgs.html#wp4769400

#### Reference ID: 1.2.2.4

##### Goal

> Under this use-case the SOC operations team would be monitoring for
> XSS attack.

##### Sources

> CISCO IDP logs

##### Requirements

1.  Configure the CISCO IDP to have updated set of cross site IPS
    signatures.\[1\]

##### Auditing to Event-ID Mapping

> N/A

##### Troubleshooting

> N/A

##### Dependency 

> N/A

##### Limitations

1.  Syslog traffic is being blocked or filtered by network and proxies.

2.  The recent patch has broken down the functionality of the syslog
    agent.

3.  If the admin exclude his / her account from auditing.

##### Affected Area

> All effected critical web-applications

##### References 

> \[1\] http://tools.cisco.com/security/center/Search.x

#### Reference ID: 1.2.2.5

##### Goal

> Under this use-case the SOC operations team would be monitoring for
> SQL injection attacks.

##### Sources

> CISCO IDP logs

##### Requirements

1.  Configure the CISCO IDP to send XSS attacks events messages in
    response to section 4.1.2.5.4

##### Auditing to Event-ID Mapping

+----------+----------+----------+------------------------------------+
| Details  |          |          |                                    |
| 1 \[1\]  |          |          |                                    |
+==========+==========+==========+====================================+
| **Pr     | AIP      |          |                                    |
| oduct:** | module   |          |                                    |
+----------+----------+----------+------------------------------------+
| **Maps   | 4.1.2.5  |          |                                    |
| to**     |          |          |                                    |
+----------+----------+----------+------------------------------------+
| S        |          | S        | Comments                           |
| ignature |          | ignature |                                    |
| ID       |          | Pack     |                                    |
+----------+----------+----------+------------------------------------+
| ###      | 3732.0   | S44      | Detects usage of a Microsoft SQL   |
| #####    |          |          | server stored procedure that is    |
| {#sectio |          |          | used to execute operating system   |
| n-1 .unn |          |          | commands                           |
| umbered} |          |          |                                    |
+----------+----------+----------+------------------------------------+
|          | 5337.0   | S47      | Detects usage of the Microsoft SQL |
|          |          |          | Server *xp_cmdshell* in the        |
|          |          |          | arguments of an HTTP request       |
+----------+----------+----------+------------------------------------+
|          | 5474.0\  | S294     | Detects the presence of encoded    |
|          | 5474.1   |          | words that are indicative of SQL   |
|          |          |          | injection attacks                  |
+----------+----------+----------+------------------------------------+
|          | 5930.0   | S349     | Detects SQL keywords in HTTP       |
|          | through  |          | arguments                          |
|          | 5930.5   |          |                                    |
+----------+----------+----------+------------------------------------+
| **S      | SQL      |          |                                    |
| ignature | I        |          |                                    |
| Title**  | NJECTION |          |                                    |
+----------+----------+----------+------------------------------------+
| **S      | Attack   |          |                                    |
| ignature |          |          |                                    |
| Type**   |          |          |                                    |
+----------+----------+----------+------------------------------------+

##### Troubleshooting steps

> N/A

##### Dependency 

> N/A

##### Limitations

> N/A

##### Affected Area

> Critical servers

##### References 

> \[1\]
> http://www.cisco.com/web/about/security/intelligence/sql_injection.html#11

### Sub-section ID: Visibility 

#### Reference ID: 1.2.3.1

##### Goal

The use case will allow the SOC team to monitor when a new port is
allowed on either inbound or outbound

##### Sources

> Cisco ASA Firewall

##### Requirements

1.  Login into the Cisco ASA firewall through console or SSH

2.  Turn on infrastructure device management access logging by running
    > the following command

+-----------------------------------------------------------------------+
| > Logging enable                                                      |
| >                                                                     |
| > Logging timestamp                                                   |
| >                                                                     |
| > logging host admin \<SIEM IP\>                                      |
+=======================================================================+
+-----------------------------------------------------------------------+

3.  Configure an offensive rule in the SIEM appliance when the following
    > type of data is observed in the firewall logs:

  -----------------------------------------------------------------------
  access-list \<name\> extended allow \<protocol\>
  \<source-network/source IP\> \<source-netmask\>
  \<destination-network/destination IP\> \<destinamtion-netmask\> eq
  \<port number\>
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details           
  ----------------- ---------------------------------------------------------
  **Product:**      Cisco ASA Firewall 5585

  **Maps to**       1.2.3.1

  **Event ID:**     

  **Event           Syslog
  Category**        

  **Event Type**    Syslog log data

  **Source:**       ASA firewall syslog data

  **Description**   This rule is generated when a user open a new port for
                    either direction (inbound/outbound) on the firewall.
  ---------------------------------------------------------------------------

##### Troubleshooting

1.  Make sure UPD 512 port is allowed between Cisco ASA firewall and
    SIEM

##### Dependency

> Cisco ASA firewall syslog data

##### Limitations

> N/A

################################################### Affected Area

> Critical firewalls

##### References 

1.  <http://www.security-solutions.co.za/cisco-asa-firewall-hardening-cisco-asa-best-practices.html>

2.  http://www.cisco.com/en/US/products/ps6120/products_configuration_example09186a0080862017.shtml

#### Reference ID: 1.2.3.2

##### Goal

This use case allows the SOC team to monitor when FTP server is accessed
from unauthorized VLAN or network.

#####  Sources

> Cisco ASA Firewall

##### Requirements

1.  Login into the Cisco ASA firewall through console or SSH

2.  Turn on syslog messages on the Cisco ASA firewall through the
    following commands:

+-----------------------------------------------------------------------+
| > Logging enable                                                      |
| >                                                                     |
| > Logging timestamp                                                   |
| >                                                                     |
| > logging host admin \<SIEM IP\>                                      |
+=======================================================================+
+-----------------------------------------------------------------------+

3.  Configure an offensive rule in the SIEM appliance when the following
    type of data is observed in the firewall logs:

  -----------------------------------------------------------------------
  %ASA-4-106100: access-list acl_ID {permitted \| denied \| est-allowed}
  protocol interface_name/source_address(source_port)(idfw_user, sg_info)
  interface_name/dest_address(dest_port) (idfw_user, sg_info) hit-cnt
  number ({first hit \| number-second interval})
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

4.  Configure an offensive rule based on the source_address field to
    generate an alert when the server is accessed from a non-trusted
    source_address (source_adddress!=trusted address)

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details           
  ----------------- ---------------------------------------------------------
  **Product:**      Cisco ASA Firewall 5585

  **Maps to**       1.2.3.4

  **Event ID:**     106100

  **Event           Syslog
  Category**        

  **Event Type**    Syslog log data

  **Source:**       ASA firewall syslog data

  **Description**   This event is generated when the ASA firewall either
                    permit or deny traffic based upon its access rule.
  ---------------------------------------------------------------------------

##### Troubleshooting

> Make sure UPD 512 port is allowed between Cisco ASA firewall and SIEM

##### Dependency

> Cisco ASA firewall syslog data

##### Limitations

> N/A

##### Affected Area

> FTP servers farm

##### References 

1.  <http://www.cisco.com/en/US/docs/security/asa/asa83/system/message/logmsgs.html#wp4769049>

2.  <http://www.cisco.com/en/US/docs/security/asa/asa90/system/message/logsevp.html>

#### Reference ID: 1.2.3.3

##### Goal

> The use case will allow the SOC team to monitor any sensitive data
> transferred over the NADRA's network.

##### Sources

> QFlow

##### Requirements

1.  On the QRadar SIEM, select the Offences tab and select the Flow
    option

2.  Create a new Flow rule and select the Source Payload option. This
    > option specifies any payload content found in the source payload.
    > Specify all the sensitive keywords we want to detect.

3.  Note the QID of the event specified in the QID field.

4.  Once the flow policy is configured look for the events associated
    with those QIDs.

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details           
  ----------------- ---------------------------------------------------------
  **Product:**      QFlow Appliance

  **Maps to**       1.2.3.5

  **Event ID:**     

  **Event           Flow Rule
  Category**        

  **Event Type**    Source Payload

  **Source:**       QFlow Flow Rule

  **Description**   This event is generated when a source payload in a packet
                    contain the keyword we specified in the rule.
  ---------------------------------------------------------------------------

#####  {#section-2 .unnumbered}

##### Troubleshooting

1.  Make sure the QFlow appliance is getting all the traffic. This is
    done through either installing the QFlow appliance inline or through
    port mirroring.

2.  Run TCPDUMP on the QFlow appliance to ensure the traffic is received
    there successfully

3.  Make sure QFlow successfully forwards the data to the QRadar SIEM
    appliance.

##### Dependency

> Network traffic, sensitive keywords classifications

##### Limitations

1.  QFlow Appliance needs to be installed inline

2.  All sensitive keywords must be defined prior to implement this rule

##### Affected Area

> Critical servers

##### References 

> QRadar User Guide Chapter 5 -- Investigating Flows

#### Reference ID: 1.2.3.4

##### Goal

This use case allows the SOC team to monitor and detect tunneled
traffic.

##### Sources

> QFlow

##### Requirements

1.  On the QRadar SIEM, select the Offences tab and select the Flow
    option

2.  Create a new Flow rule and select the Protocol option and choose the
    protocol for which we want to configure the rule. For example, if we
    want to detect FTP data tunneled over HTTP, select HTTP in this
    step.

3.  Choose the Custom Rule option to create a custom rule for the flow.

4.  Select the Payload option and generate an offense when payload is
    not equal to protocol.

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details 1         
  ----------------- ---------------------------------------------------------
  **Product:**      QFlow Appliance

  **Maps to**       1.2.3.6

  **Event ID:**     

  **Event           Flow Rule
  Category**        

  **Event Type**    Protocol

  **Source:**       QFlow Flow Rule

  **Description**   This event is generated when payload of a packet doesn't
                    correspond to the protocol specified in the Protocol
                    field.
  ---------------------------------------------------------------------------

##### Troubleshooting

1.  Make sure the QFlow appliance is getting all the traffic. This is
    done through either installing the QFlow appliance inline or through
    port mirroring.

2.  Run TCPDUMP on the QFlow appliance to ensure the traffic is received
    there successfully

3.  Make sure QFlow successfully forwards the data to the QRadar SIEM
    appliance.

##### Dependency

> Network traffic

##### Limitations

> QFlow Appliance needs to be installed inline or configured through
> port mirroring

##### Affected Area

> Across all NADRA vlans

##### References 

> QRadar User Guide Chapter 5 -- Investigating Flows

#### Reference ID: 1.2.3.5

##### Goal

> This use case allow the SOC team to monitor when a new user is created
> on the Juniper / Cisco ASA firewall

##### Sources

> Cisco ASA Firewall AND Juniper

##### Requirements

1.  Login into the Cisco ASA firewall through console or SSH

2.  Turn on infrastructure device management access logging by running
    the following command

+-----------------------------------------------------------------------+
| > Logging enable                                                      |
| >                                                                     |
| > Logging timestamp                                                   |
| >                                                                     |
| > logging host admin \<SIEM IP\>                                      |
+=======================================================================+
+-----------------------------------------------------------------------+

3.  Configure an offensive rule in the SIEM appliance when the following
    type of data is observed in the firewall logs:

+-----------------------------------------------------------------------+
| > %ASA-5-502101: New user added to local dbase: Uname: user Priv:     |
| > privilege_level Encpass: string                                     |
+=======================================================================+
+-----------------------------------------------------------------------+

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details           
  ----------------- ---------------------------------------------------------
  **Product:**      Cisco ASA Firewall 5585

  **Maps to**       1.2.3.7

  **Event ID:**     502101

  **Event           Syslog
  Category**        

  **Event Type**    Syslog log data

  **Source:**       ASA firewall syslog data

  **Description**   This rule is generated when a new user account is created
                    on the ASA firewall
  ---------------------------------------------------------------------------

##### Troubleshooting

> Make sure UPD 512 port is allowed between Cisco ASA firewall and SIEM

##### Dependency

> Cisco ASA firewall syslog data

##### Affected Area

> Critical servers

##### Limitations

> N/A

##### References 

1.  http://www.cisco.com/en/US/docs/security/asa/asa83/system/message/logmsgs.html#wp4773963

#### Reference ID: 1.2.3.6

##### Goal

> This use case will allow the SOC team to monitor when data is uploaded
> to the Internet in RAR archive chunks.

##### Sources

> QFlow

##### Requirements

1.  On the QRadar SIEM, select the Offences tab and select the Flow
    option

2.  Create a new Flow rule and select the Source Payload option. This
    option specifies any payload content found in the source payload.
    Specify all the sensitive keywords we want to detect.

3.  Select the Custom Rule option and configure a custom rule when the
    Source Payload contain "RAR!\..." payload

4.  Select the Source Byte greater than 20 MB.

5.  Note the QID of the event specified in the QID field.

6.  Once the flow policy is configured look for the events associated
    with those QIDs.

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details           
  ----------------- ---------------------------------------------------------
  **Product:**      QFlow Appliance

  **Maps to**       1.2.3.8

  **Event ID:**     

  **Event           Flow Rule
  Category**        

  **Event Type**    Source Payload, Source Byte

  **Source:**       QFlow Flow Rule

  **Description**   This event is generated when the source payload contain
                    the specified application data
  ---------------------------------------------------------------------------

##### Troubleshooting

1.  Make sure the QFlow appliance is getting all the traffic. This is
    done through either installing the QFlow appliance inline or through
    port mirroring.

2.  Run TCPDUMP on the QFlow appliance to ensure the traffic is received
    there successfully1Make sure QFlow successfully forwards the data to
    the QRadar SIEM appliance.

##### Dependency

> N/A

##### Limitations

1.  QFlow Appliance needs to be installed inline or configured through
    port mirror

2.  The rule is going to trigger only when the source byte is greater
    than 20 MB. We assumed the email attachment size is 20 MB that is
    why the user is going to use the Internet upload option. If the
    source bytes are less than 20 MB (in other words if the uploaded
    data is less than 20 MB), the rule will not be triggered.

##### Affected Area

> All NADRA vlans

##### References 

> QRadar User Guide Chapter 5 -- Investigating Flows

#### Reference ID: 1.2.3.7

##### Goal

> This use case will allow the SOC team to monitor when an online
> messenger is used to chat or transfer files.

##### Sources

> QFlow

##### Requirements

1.  On the QRadar SIEM, select the Offences tab and select the Flow
    option

2.  Create a new Flow rule and select the Source Payload option. This
    option specifies any payload content found in the source payload.
    Specify all the sensitive keywords we want to detect.

3.  Select the Custom Rule option and configure a custom rule when the
    Source Payload contain "IMP (instant message applications)\..."
    payload

##### Auditing to Event-ID Mapping

> N/A

##### Troubleshooting

1.  Make sure the QFlow appliance is getting all the traffic. This is
    done through either installing the QFlow appliance inline or through
    port mirroring.

2.  Run TCPDUMP on the QFlow appliance to ensure the traffic is received
    there successfully1Make sure QFlow successfully forwards the data to
    the QRadar SIEM appliance.

##### Dependency

> N/A

##### Limitations

> N/A

##### Affected Area

> All NADRA vlans

##### References 

> \[1\]
> <http://www.ndm.net/siem/pdf/q1labs/The-Value-of-QRadar-QFlow-and-QRadar->VFlow-for-Security-Intelligence.pdf

#### Reference ID: 1.2.3.8

##### Goal

> This use case will allow the SOC team to monitor when malicious
> traffic hit the executive network

##### Sources

> Cisco ASA 5585 Firewall AIP Module

##### Requirements

1.  Login into the Cisco ASA firewall through console or SSH

2.  Turn on infrastructure device management access logging by running
    the following command

3.  Configure Cisco Intrusion Prevention Systems (forensics) DSM in the
    QRadar.

4.  Configure an offensive rule based on the destination_address field
    to generate an alert when destination_address contain one of the IP
    address assigned to the executive subnet.

5.  Step by step procedure of how to turn on packet inspection is given
    at
    <http://www.cisco.com/en/US/products/ps6120/products_configuration_example09186a00807335ca.shtml>

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details 1         
  ----------------- ---------------------------------------------------------
  **Product:**      Cisco ASA Firewall 5585

  **Maps to**       1.2.3.4

  **Event ID:**     106100

  **Event           Syslog
  Category**        

  **Event Type**    Syslog log data

  **Source:**       ASA firewall syslog data

  **Description**   This event is generated when the ASA firewall either
                    permit or deny traffic based upon its access rule.
  ---------------------------------------------------------------------------

##### Troubleshooting

> Using the CISCO OIT (Output Interpreter Tool), issue the following
> "show" commands to troubleshoot. The following show commands are
> helpful in troubleshooting the problem:

a.  Show module

b.  Show run

c.  Show access-list

> Further troubleshooting details are available at References
> section.\[3\]

##### Dependency

> Cisco ASA firewall syslog data

##### Limitations

> N/A

##### Affected Area

> All such secure vlans

##### References 

1.  <http://www.cisco.com/en/US/docs/security/asa/asa83/system/message/logmsgs.html#wp4769049>

2.  http://www.cisco.com/en/US/docs/security/asa/asa90/system/message/logsevp.html

3.  http://www.cisco.com/en/US/products/ps6120/products_configuration_example09186a00807335ca.shtml

#### Reference ID: 1.2.3.9

##### Goal

> This use case will enable SOC team to monitor the event when SIP
> phones receive telnet traffic.

##### Sources

> Cisco ASA Firewall

##### Requirements

1.  Login into the Cisco ASA firewall through console or SSH

2.  Turn on syslog messages on the Cisco ASA firewall through the
    following commands:

+-----------------------------------------------------------------------+
| > Logging enable                                                      |
| >                                                                     |
| > Logging timestamp                                                   |
| >                                                                     |
| > logging host admin \<SIEM IP\>                                      |
+=======================================================================+
+-----------------------------------------------------------------------+

3.  Configure an offensive rule in the SIEM appliance when the following
    type of data is observed in the firewall logs:

  -----------------------------------------------------------------------
  %ASA-4-106100: access-list acl_ID {permitted \| denied \| est-allowed}
  protocol interface_name/source_address(source_port)(idfw_user, sg_info)
  interface_name/dest_address(23) (idfw_user, sg_info) hit-cnt number
  ({first hit \| number-second interval})
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

4.  Configure an offensive rule based on the dest_address and dest_port
    fields to generate an alert when dest_address is one of the SIP
    phone IP addresses and destination port is 23 which is the default
    telnet port.

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details 1         
  ----------------- ---------------------------------------------------------
  **Product:**      Cisco ASA Firewall 5585

  **Maps to**       1.2.3.8

  **Event ID:**     106100

  **Event           Syslog
  Category**        

  **Event Type**    Syslog log data

  **Source:**       ASA firewall syslog data

  **Description**   This event is generated when the ASA firewall either
                    permit or deny traffic based upon its access rule.
  ---------------------------------------------------------------------------

##### Troubleshooting

> Make sure UPD 512 port is allowed between Cisco ASA firewall and SIEM

##### Dependency

> Cisco ASA firewall syslog data

##### Limitations

> N/A

##### Affected Area

> All sip devices/ phones / servers

##### References 

1.  <http://www.cisco.com/en/US/docs/security/asa/asa83/system/message/logmsgs.html#wp4769049>

2.  <http://www.cisco.com/en/US/docs/security/asa/asa90/system/message/logsevp.html>

#### Reference ID: 1.2.3.10

##### Goal

> This use case will enable the SOC team when attempt is made to access
> adult contents from the NADRA's protected network.

##### Sources

> Microsoft TMG Proxy

##### Requirements

1.  Configure URL Filtering in the right pane of the ISA management
    console

2.  Click on the Category Query and Select the Liability category.
    Pornography and adult contents are sub category of Liability

3.  Check the Liability category and press OK

4.  Install QRadar Adaptive Log Exporter (ALE) agent on the ISA proxy
    server

5.  Open the ALE interface and select the ISA Server. In the
    RootLogDirectory field, enter C:\\Windows\\System32\\LogFiles and
    press OK. ALE will gather the TMG Logs from the specified directory.

6.  Create an offensive rule to fire when logs in the TMG proxy logs
    contain Category=Liability and Sub Category=Pornography

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details 1         
  ----------------- ---------------------------------------------------------
  **Product:**      Cisco ASA Firewall 5585

  **Maps to**       1.2.3.7

  **Event ID:**     \-

  **Event           Windows Logs
  Category**        

  **Event Type**    QRadar Adaptive Log Exporter Logs

  **Source:**       Microsoft TMG Proxy Server

  **Description**   This event is generated when the Microsoft TMG Proxy
                    block a pornographic URL request
  ---------------------------------------------------------------------------

##### Troubleshooting

1.  Make sure the ALE agent is able to communicate with the QRadar SIEM
    > and logs are successfully received at the QRadar SIEM console.

2.  Verify that TMG is logging the events when URL is blocked based on
    > some category.

##### Dependency

1.  Logs are enabled and TMG Proxy

2.  ALE transfer logs from the TMG Proxy to the QRadar SIEM

##### Limitations

> N/A

##### Affected Area

> All vlans effected

##### References 

1.  <http://www.isaserver.org/tutorials/TMG-Back-Basics-Part8.html>

#### Reference ID: 1.2.3.11

##### Goal

> This use case will enable SOC team to monitor when someone perform
> port scan against the SIP ports 5060 and 5061.

##### Sources

> Cisco ASA Firewall

##### Requirements

1.  Login into the Cisco ASA firewall through console or SSH

2.  Turn on syslog messages on the Cisco ASA firewall through the
    following commands:

+-----------------------------------------------------------------------+
| > Logging enable                                                      |
| >                                                                     |
| > Logging timestamp                                                   |
| >                                                                     |
| > logging host admin \<SIEM IP\>                                      |
+=======================================================================+
+-----------------------------------------------------------------------+

3.  Configure an offensive rule in the SIEM appliance when the following
    type of data is observed in the firewall logs:

  -----------------------------------------------------------------------
  %ASA-4-106100: access-list acl_ID {permitted \| denied \| est-allowed}
  protocol interface_name/source_address(source_port)(idfw_user, sg_info)
  interface_name/dest_address(5060\|5061) (idfw_user, sg_info) hit-cnt
  number ({first hit \| number-second interval})
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

4.  Configure an offensive rule based on the number of such events. A
    threshold of 5 can be set to fire the offensive rule when five
    connection attempts are detected in 1 second of time.

##### Auditing to Event-ID Mapping

  ---------------------------------------------------------------------------
  Details 1         
  ----------------- ---------------------------------------------------------
  **Product:**      Cisco ASA Firewall 5585

  **Maps to**       1.2.3.9

  **Event ID:**     106100

  **Event           Syslog
  Category**        

  **Event Type**    Syslog log data

  **Source:**       ASA firewall syslog data

  **Description**   This event is generated when the ASA firewall either
                    permit or deny traffic based upon its access rule.
  ---------------------------------------------------------------------------

##### Troubleshooting

> Make sure UPD 512 port is allowed between Cisco ASA firewall and SIEM

##### Dependency

> Cisco ASA firewall syslog data

##### Limitations

> N/A

##### Affected Area

> All sip devices/ phones / servers

##### References 

1.  <http://www.cisco.com/en/US/docs/security/asa/asa83/system/message/logmsgs.html#wp4769049>

2.  http://www.cisco.com/en/US/docs/security/asa/asa90/system/message/logsevp.html

### Sub-section ID: Policy violations 

#### Reference ID: 1.2.4.1 

##### Goal

> Under this use-case the SOC operations team would be monitoring for
> detecting bit-torrent traffic over network

##### Sources

> Qflows device,CISCO IDP (ASA)

##### Requirements

1.  Configure the cisco ASA device to send logs related to bit-torrent
    events.

##### Auditing to Event-ID Mapping

  -----------------------------------------------------------------------------
  Details 1 \[1\]   
  ----------------- -----------------------------------------------------------
  **Product:**      AIP module

  **Maps to**       4.1.3.1.3

  **Event ID:**     11030/0

  **Description**   BitTorrent is a P2P file sharing program designed to
                    quickly disseminate files in a distributed fashion. This
                    network is relying on the presence of trackers to
                    synchronize the file status
  -----------------------------------------------------------------------------

##### Troubleshooting

> Make sure UPD 512 port is allowed between **Cisco ASA firewall** and
> SIEM

##### Dependency 

> N/A

##### Limitations

> 1\. CISCO asa events are cleared before being send to Qradar appliance
> (SIEM server)

##### Affected Area

> All NADRA vlans

##### References 

> \[1\]http://tools.cisco.com/security/center/viewIpsSignature.x?signatureId=11030&signatureSubId=0

#### Reference ID: 1.2.4.2

##### Goal

Under this use-case the SOC operations team would be monitoring for
firewall admin saves config file on an unauthorized machine.

##### Sources

> CISCO IDP (ASA) and juniper

##### Requirements

> CISCO ASA is configured to view events related to configuration
> action. To configure set the ASA to send logs related to message ID
> 111008 and 111010. The syslog number 111008 and 111010 will log the
> command that is entered by user.

##### Auditing to Event-ID Mapping

  -----------------------------------------------------------------------------
  Details 1 \[1\]   
  ----------------- -----------------------------------------------------------
  **Product:**      ASA

  **Maps to**       4.1.4.2

  **Event ID:**     111008

  **Description**   BitTorrent is a P2P file sharing program designed to
                    quickly disseminate files in a distributed fashion. This
                    network is relying on the presence of trackers to
                    synchronize the file status

  Details 2 \[1\]   

  **Product:**      ASA

  **Maps to**       4.1.4.2

  **Event ID:**     111010

  **Description**   BitTorrent is a P2P file sharing program designed to
                    quickly disseminate files in a distributed fashion. This
                    network is relying on the presence of trackers to
                    synchronize the file status
  -----------------------------------------------------------------------------

##### Troubleshooting

> Make sure UPD 512 port is allowed between **Cisco ASA firewall** and
> SIEM

##### Dependency 

> N/A

##### Limitations

> N/A

##### Affected Area

> All such network devices

##### References 

> \[1\]www.cisco.com/en/US/docs/security/asa/asa84/system/message/logmsgs.html#wp4769410

### Sub-section ID: Operations

#### Reference ID: 1.2.5.1

##### Goal

> Under this use-case the SOC operations team would be monitoring for If
> X number of changes have been made on a firewall over x period of time
> by x user.

##### Sources

> CISCO IDP (ASA)

##### Requirements

CISCO ASA is configured to view events related to configuration action.
Events would be matched as follows:-

1.  Time differences between most recent changes to firewall are alerted
    when exceeded beyond set limit.

> Changes made in x time -- Changes made in y time.

##### Auditing to Event-ID Mapping

  -----------------------------------------------------------------------------
  Details 1 \[1\]   
  ----------------- -----------------------------------------------------------
  **Product:**      AIP module

  **Maps to**       4.1.5.1

  **Event ID:**     111008

  **Description**   BitTorrent is a P2P file sharing program designed to
                    quickly disseminate files in a distributed fashion. This
                    network is relying on the presence of trackers to
                    synchronize the file status

  Details 2 \[1\]   

  **Product:**      AIP module

  **Maps to**       4.1.5.1

  **Event ID:**     111010

  **Description**   BitTorrent is a P2P file sharing program designed to
                    quickly disseminate files in a distributed fashion. This
                    network is relying on the presence of trackers to
                    synchronize the file status
  -----------------------------------------------------------------------------

##### Troubleshooting 

> N/A

##### Dependency 

> N/A

##### Limitations

> N/A

##### Affected Area

> All such network devices

##### References 

> \[1\]www.cisco.com/en/US/docs/security/asa/asa84/system/message/logmsgs.html#wp4769410

### Sub-section ID: Legal

#### Reference ID: 1.2.6.1

##### Goal

> Under this use-case the SOC operations team would be monitoring for If
> a disgruntled employee launches an attack to outside agency using
> NADRA network.

##### Sources

> CISCO IDP (ASA)

##### Requirements

1.  Login into the Cisco ASA firewall through console or SSH

2.  Turn on infrastructure device management access logging by running
    the following command

+-----------------------------------------------------------------------+
| > Logging enable                                                      |
| >                                                                     |
| > Logging timestamp                                                   |
| >                                                                     |
| > logging host admin \<SIEM IP\>                                      |
+=======================================================================+
+-----------------------------------------------------------------------+

3.  Configure an offensive rule in the SIEM appliance when the following
    type of data is observed in the firewall logs:

  -----------------------------------------------------------------------
  access-list \<name\> extended allow \<protocol\>
  \<source-network/source IP\> \<source-netmask\>
  \<destination-network/destination IP\> \<destinamtion-netmask\> eq
  \<port number\>
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

##### Auditing to Event-ID Mapping

  -----------------------------------------------------------------------------
  Details 1 \[1\]   
  ----------------- -----------------------------------------------------------
  **Product:**      AIP module

  **Maps to**       4.1.5.1

  **Event ID:**     111008

  **Description**   BitTorrent is a P2P file sharing program designed to
                    quickly disseminate files in a distributed fashion. This
                    network is relying on the presence of trackers to
                    synchronize the file status
  -----------------------------------------------------------------------------

  -----------------------------------------------------------------------------
  Details 2 \[1\]   
  ----------------- -----------------------------------------------------------
  **Product:**      AIP module

  **Maps to**       4.1.5.1

  **Event ID:**     111010

  **Description**   BitTorrent is a P2P file sharing program designed to
                    quickly disseminate files in a distributed fashion. This
                    network is relying on the presence of trackers to
                    synchronize the file status
  -----------------------------------------------------------------------------

##### Troubleshooting 

> N/A

##### Dependency 

> N/A

##### Limitations

> N/A

##### Affected Area

> All such network devices

##### References 

> \[1\]www.cisco.com/en/US/docs/security/asa/asa84/system/message/logmsgs.html#wp4769410
