# Wazuh Rule Analysis

This document explains how each custom rule works, why it matters, and which
attack technique it detects.

## Excessive Failed Logons (Rule 100001)

Detects brute-force or password spraying attempts by counting failed logons
within a timeframe.

## Event Log Clearing (Rule 100002)

Detects Event ID 1102, which indicates the Security log was cleared — a common
defense evasion technique.

## Suspicious PowerShell (Rule 100003)

Detects encoded PowerShell commands, often used for obfuscation.

