# Mock Data Generator
![Python](https://img.shields.io/badge/Python-3.11-blue)
![PDM](https://img.shields.io/badge/PDM-2.19.2-green)

This project is a Python-based utility designed to generate mock data for various use cases, such as testing, prototyping, and demonstrations. The generator dynamically creates data based on a customizable JSON schema, making it versatile for multiple domains and scenarios.

## Key Features

- **Dynamic Schema Support:**
  - Accepts a JSON schema to define the structure, data types, and constraints of the generated data.
  - Supports a wide variety of data types, including integers, decimals, text, dates, emails, and enums.

- **Enum Field Generation:**
  - Generates random values from a predefined set of options for fields marked as enums.

- **Flexible Constraints:**
  - Allows configuration of minimum and maximum ranges for numeric and decimal fields.
  - Supports variable-length text fields.

- **Realistic Data:**
  - Leverages the `Faker` library to produce realistic and meaningful mock data, such as names, cities, phone numbers, and email addresses.

- **Excel Export:**
  - Outputs the generated data directly to an Excel file for easy integration and analysis.

## Supported Field Types

- **Integer (`int`):**
  Generates random integers within a specified range (`min` and `max`).

- **Decimal (`decimal`):**
  Produces random floating-point numbers with optional precision and range constraints.

- **Variable-Length Text (`varchar`):**
  Creates text fields with a maximum character length.

- **Dates (`date`):**
  Generates random dates within the current decade.

- **Email (`email`):**
  Generates realistic email addresses.

- **Phone (`phone`):**
  Produces formatted phone numbers.

- **City (`city`) and Country (`country`):**
  Generates realistic city and country names.

- **Name (`name`):**
  Produces full names of individuals.

- **Enum (`enum`):**
  Randomly selects values from a predefined list of options.

## Example Use Cases

- Testing and validating software applications with realistic datasets.
- Prototyping dashboards, charts, and visualizations for data-centric tools.
- Demonstrating functionalities in data analysis, recruitment platforms, or e-commerce systems.

## Example Schema

```json
{
  "CandidateID": {"type": "int", "options": {"min": 1, "max": 1000}},
  "Name": {"type": "name"},
  "Email": {"type": "email"},
  "Phone": {"type": "phone"},
  "City": {"type": "city"},
  "Country": {"type": "country"},
  "ExperienceYears": {"type": "decimal", "options": {"min": 0, "max": 20}},
  "AppliedDate": {"type": "date"},
  "Status": {"type": "enum", "options": {"options": ["Applied", "Interviewing", "Hired", "Rejected"]}}
}
```

## Benefits

- **Customizability:** Fully adaptable to specific data requirements through JSON schema.
- **Realism:** Provides believable mock data for diverse scenarios.
- **Ease of Use:** Generates data in structured formats, ready for analysis or use in other applications.

## Dependencies

- `Faker`: Used for generating realistic names, dates, emails, and other fields.
- `pandas`: For structuring data and exporting it to Excel.
- `random`: Used for creating random numbers and selecting options from enums.

## Limitations

- The generator currently supports a predefined set of field types. Extending the field types requires code modification.
- Enum fields must have their options explicitly defined in the schema.

---

This project is ideal for developers, data scientists, and testers who need quick, realistic datasets tailored to their specific needs.

