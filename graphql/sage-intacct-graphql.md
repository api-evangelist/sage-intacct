# Sage Intacct GraphQL Schema

## Overview

This conceptual GraphQL schema represents the Sage Intacct cloud financial management data model. Sage Intacct exposes its data through a REST API (OAuth 2.0) and a legacy XML API. This schema maps those capabilities into a unified GraphQL type system covering the full breadth of the platform: general ledger, accounts payable, accounts receivable, cash management, project accounting, purchasing, order entry, dimensions, and platform services.

Reference: https://developer.intacct.com/api/

## Core Domains

### General Ledger
Types covering chart of accounts, journal entries, budgets, and financial reporting. GL accounts are organized into account groups and posted through journals. Budget and forecast entries track planned versus actual values. Reporting types expose aging, trial balance, and custom financial report definitions.

### Accounts Payable
Vendors, AP bills, AP payments, AP credits, and aged payables. Tracks the full lifecycle of vendor invoices from receipt through payment.

### Accounts Receivable
Customers, AR invoices, AR payments, AR credits, cash receipts, and aged receivables. Covers the full revenue collection cycle.

### Cash Management
Bank accounts, bank feeds, deposits, cash entries, and advanced credits. Supports multi-entity cash positions and bank reconciliation.

### Project Accounting
Projects, tasks, timesheets, timesheet entries, employee expenses, expense lines, project contracts, and project resources. Supports time and expense capture, billing, and project-based revenue recognition.

### Purchasing and Order Entry
Purchase orders (PODocument, POTransaction), sales orders (SODocument, SOTransaction), and associated line items. Integrates with inventory items and vendor/customer master data.

### Dimensions and Configuration
Locations, departments, classes, functions, and custom dimensions with dimension values. Restrictions control which dimension combinations are valid. Company preferences and API tokens support platform configuration.

### Platform Services
Webhooks, API connections, custom fields, and integration tokens provide extensibility and automation hooks.

## Schema Source

Derived from Sage Intacct developer documentation and data model:
- REST API: https://developer.sage.com/intacct/docs/1/sage-intacct-rest-api/
- XML API: https://developer.intacct.com/api/
- GitHub: https://github.com/Intacct

## Type Count

This schema defines 68 named GraphQL types (object types, enums, input types, and scalars).
