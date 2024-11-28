# RAW PostgreSQL Integration API Template

## Table of Contents

1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Endpoint](#endpoint)
4. [Short Intro to RAW APIs](#short-intro-to-raw-apis)
5. [Next Steps](#next-steps)
6. [License](#license)
7. [Contact](#contact)

---

## Introduction

This repository provides a **PostgreSQL Integration API Template** using the RAW Labs platform. It demonstrates how to create an API endpoint that connects to your PostgreSQL database and executes SQL queries. This template serves as a starting point for building APIs that interact with your own database schema.

**This template is a foundational base that you can customize to fit your needs.** The provided placeholder SQL query returns a simple greeting message, but you are encouraged to replace it with any valid SQL query against your PostgreSQL database. **By customizing the query, you can retrieve data from your specific tables and views, enabling you to build powerful APIs tailored to your unique requirements.**

## Getting Started

1. **Deploy the API:**
   - Visit the [Data Sharing PostgreSQL Starter Template](https://www.raw-labs.com/templates/data-sharing-postgresql-starter).
   - Click the **"Get Started"** button to deploy the template.
   - If you don’t have a RAW account, you’ll be prompted to create one for free. Deployment and account setup are seamless—just one click away!

2. **Explore the API:**
   - Access your API immediately inside the RAW application.
   - View endpoint details and invoke them directly to see how they function.

3. **Customize as Needed:**
   - Modify the API to suit your requirements.
   - Once you’re satisfied, re-publish the changes to make your new API available instantly.

## Endpoint

### **GET `/postgresql/query`**

- **Description**: Retrieves a greeting message 'Hello, World!' as a result of the SQL query. This is a placeholder SQL query. You can replace this query with any valid SQL query against your PostgreSQL database.
- **Query Parameters**: None by default (can be added if you customize the query).
- **Source Code**:
  - SQL Query: [/postgresql/query.sql](./postgresql/query.sql)
  - Endpoint Definition: [/postgresql/query.yml](./postgresql/query.yml)

**Example Default Response**:

```json
[
  {
    "greeting": "Hello, World!"
  }
]
```

## Short Intro to RAW APIs

In RAW, APIs consist of two parts: a YAML file for endpoint configuration and a SQL file for the query logic. The YAML file path defines the API’s endpoint. For example, /postgresql/query.yml corresponds to the API path /postgresql/query.

SQL queries can include dynamic parameters using the `:<variable_name>` syntax. For instance:
```sql
WHERE CustomerID = :customer_id
```
Here, `:customer_id` becomes a query parameter, accessible via the API as `?customer_id=<value>`.

To document parameters, enforce types or default values, add metadata at the top of the SQL file as in:
```sql
-- @param customer_id the ID of the customer  
-- @type customer_id integer  
-- @default customer_id null
```

## Next Steps

Visit the [Data Sharing PostgreSQL Starter Template](https://www.raw-labs.com/templates/data-sharing-postgresql-starter) page, deploy this template and get started using RAW.

When you create your RAW account, you will be able to view and run these endpoints in the RAW catalog, as well as quickly modify these endpoints or create new ones in the RAW workspace, in our easy-to-use web IDE.

## License

This project is licensed under the **Apache License 2.0**. See the [LICENSE](LICENSE) file for details.

## Contact

- **Website**: [www.raw-labs.com](https://www.raw-labs.com)
- **Twitter**: [@raw_labs](https://twitter.com/raw_labs)
- **Contact Support**: Email us at [support@raw-labs.com](mailto:support@raw-labs.com) for assistance
- **Community Forum**: Join the discussion on our [Community Forum](https://www.raw-labs.com/community)

For more information, visit our [documentation](https://docs.raw-labs.com).
