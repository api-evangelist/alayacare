# AlayaCare (api-evangelist-alayacare)

AlayaCare is a cloud-based home and community care management platform providing REST APIs for managing client profiles, scheduling visits, documenting clinical care, processing billing and accounting, and tracking patient outcomes. The platform serves home care agencies, nursing registries, and government-funded community care programs globally. APIs cover clients, employees, scheduling, clinical records, tasks, forms, medications, accounting, and file management, with integration via REST and AWS SQS event streaming. AlayaCare also offers AlayaMarket, a staffing marketplace API for matching supply and demand organizations, and AlayaCare Residential for residential aged care settings.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/alayacare/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/alayacare/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Home Care
- Community Care
- Healthcare
- Scheduling
- Clinical
- Billing
- Client Management
- Care Management
- Aged Care
- Workforce Management

## Timestamps

- **Created:** 2026-06-13
- **Modified:** 2026-06-13

## APIs

### AlayaCare Client API

REST API for managing client (patient) profiles in AlayaCare, including demographics, contact information, care groups, and client-level metadata. Supports creating, retrieving, and updating patient records. Authenticated via HTTP Basic Auth using tenant-specific public/private key pairs provisioned by AlayaCare.

- **Human URL:** [https://alayacare.github.io/external-integration-docs/external-api-guide.html](https://alayacare.github.io/external-integration-docs/external-api-guide.html)
- **Base URL:** `https://[tenant].[environment].alayacare.[domain]/ext/api/v2/patients/`

#### Tags

- Clients
- Patients
- Demographics

#### Properties

- [Documentation](https://alayacare.github.io/external-integration-docs/external-api-guide.html)
- [OpenAPI](https://app.swaggerhub.com/apis/AlayaCare/client-api-external) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### AlayaCare Employee API

REST API for managing employee records including staff information, designations, departments, and employee-level attributes. Enables HR and workforce management integrations. Supports pagination and date-range filtering. Authentication uses HTTP Basic Auth with tenant-specific credentials.

- **Human URL:** [https://alayacare.github.io/external-integration-docs/external-api-guide.html](https://alayacare.github.io/external-integration-docs/external-api-guide.html)
- **Base URL:** `https://[tenant].[environment].alayacare.[domain]/ext/api/v2/employees/`

#### Tags

- Employees
- Workforce
- HR

#### Properties

- [Documentation](https://alayacare.github.io/external-integration-docs/external-api-guide.html)

### AlayaCare Scheduler API

REST API for accessing and managing visit scheduling data, including visit details, facility information, and service delivery records. Supports filtering by date range and pagination. Critical for building scheduling integrations, rostering tools, and payroll system connectors.

- **Human URL:** [https://alayacare.github.io/external-integration-docs/external-api-guide.html](https://alayacare.github.io/external-integration-docs/external-api-guide.html)
- **Base URL:** `https://[tenant].[environment].alayacare.[domain]/ext/api/v2/scheduler/`

#### Tags

- Scheduling
- Visits
- Rostering

#### Properties

- [Documentation](https://alayacare.github.io/external-integration-docs/external-api-guide.html)

### AlayaCare Clinical API

REST API for accessing clinical documentation including progress notes, medications, vital signs, and clinical observations recorded during care visits. Supports integration with EMR/EHR systems and clinical data warehouses. Authenticated via HTTP Basic Auth with tenant-scoped credentials.

- **Human URL:** [https://alayacare.github.io/external-integration-docs/external-api-guide.html](https://alayacare.github.io/external-integration-docs/external-api-guide.html)
- **Base URL:** `https://[tenant].[environment].alayacare.[domain]/ext/api/v2/clinical/`

#### Tags

- Clinical
- Progress Notes
- Vitals
- Medications

#### Properties

- [Documentation](https://alayacare.github.io/external-integration-docs/external-api-guide.html)

### AlayaCare Tasks API

REST API (v1 and v2) for managing care tasks assigned to clients and employees within AlayaCare. Supports creating, retrieving, and updating task records. Tasks v2 adds expanded capabilities. Used for workflow automation and care coordination integrations.

- **Human URL:** [https://alayacare.github.io/external-integration-docs/external-api-guide.html](https://alayacare.github.io/external-integration-docs/external-api-guide.html)
- **Base URL:** `https://[tenant].[environment].alayacare.[domain]/ext/api/v2/tasks/`

#### Tags

- Tasks
- Care Coordination
- Workflow

#### Properties

- [Documentation](https://alayacare.github.io/external-integration-docs/external-api-guide.html)

### AlayaCare Forms API

REST API for accessing digital form submissions captured during care delivery, including assessment forms, intake forms, and clinical documentation forms. Updated November 2024 with Forms v2 support. Enables reporting, compliance, and quality assurance integrations.

- **Human URL:** [https://alayacare.github.io/external-integration-docs/external-api-guide.html](https://alayacare.github.io/external-integration-docs/external-api-guide.html)
- **Base URL:** `https://[tenant].[environment].alayacare.[domain]/ext/api/v2/tasks/forms20`

#### Tags

- Forms
- Assessments
- Documentation

#### Properties

- [Documentation](https://alayacare.github.io/external-integration-docs/external-api-guide.html)

### AlayaCare Accounting API

REST API for financial operations within AlayaCare, including billing records, invoices, and accounting data. Supports integration with payroll systems, financial reporting tools, and ERP platforms. Authenticated via HTTP Basic Auth with tenant credentials.

- **Human URL:** [https://alayacare.github.io/external-integration-docs/external-api-guide.html](https://alayacare.github.io/external-integration-docs/external-api-guide.html)
- **Base URL:** `https://[tenant].[environment].alayacare.[domain]/ext/api/v2/`

#### Tags

- Billing
- Accounting
- Finance

#### Properties

- [Documentation](https://alayacare.github.io/external-integration-docs/external-api-guide.html)

### AlayaCare Medication API

REST API for managing medication records associated with client care plans in AlayaCare. Supports retrieval of medication lists, dosage information, and administration records for integration with pharmacy systems and medication management platforms.

- **Human URL:** [https://alayacare.github.io/external-integration-docs/external-api-guide.html](https://alayacare.github.io/external-integration-docs/external-api-guide.html)
- **Base URL:** `https://[tenant].[environment].alayacare.[domain]/ext/api/v2/`

#### Tags

- Medications
- Pharmacy
- Clinical

#### Properties

- [Documentation](https://alayacare.github.io/external-integration-docs/external-api-guide.html)

### AlayaMarket Marketplace API

REST API for the AlayaMarket staffing marketplace enabling supply and demand organizations to exchange shift offers and staffing requests. Demand organizations use Outbox APIs to publish staffing needs; supply organizations use Inbox APIs to respond. Supports both synchronous REST and asynchronous AWS SNS event notifications. Available in three regions: Australia, Canada, and USA with sandbox environments.

- **Human URL:** [https://alayacare.github.io/alayamarket-external-docs/docs/user_guide/](https://alayacare.github.io/alayamarket-external-docs/docs/user_guide/)
- **Base URL:** `https://api.prod.alayacare.com`

#### Tags

- Marketplace
- Staffing
- Workforce
- Shift Management

#### Properties

- [Documentation](https://alayacare.github.io/alayamarket-external-docs/docs/user_guide/)
- [Git Hub](https://github.com/AlayaCare/alayamarket-external-docs)

### AlayaCare Residential (Resi) API

REST API for AlayaCare's residential aged care product, supporting client extensions, resident management, and care documentation specific to residential facility settings. Separate from the home care APIs; hosted at residential.alayacare.com.au with dedicated API documentation.

- **Human URL:** [https://acresi-api-docs.residential.alayacare.com/](https://acresi-api-docs.residential.alayacare.com/)
- **Base URL:** `https://residential.alayacare.com.au/api/`

#### Tags

- Residential
- Aged Care
- Client Extensions

#### Properties

- [Documentation](https://acresi-api-docs.residential.alayacare.com/)

## Common Properties

- [Website](https://alayacare.com/)
- [Documentation](https://alayacare.github.io/external-integration-docs/)
- [Git Hub](https://github.com/alayacare)
- [LinkedIn](https://www.linkedin.com/company/alayacare/)
- [Blog](https://alayacare.com/blog/)
- [Integrations Brochure](https://alayacare.com/brochures/alayacare-integrations-and-apis/)
- [A P I Terms](https://alayacare.com/wp-content/uploads/2022/12/AlayaCare-API-Developer-Access-Terms-.pdf)
- [Plans](plans/alayacare-plans-pricing.yml)
- [Rate Limits](rate-limits/alayacare-rate-limits.yml)
- [Fin Ops](finops/alayacare-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
