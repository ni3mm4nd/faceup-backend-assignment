# Database design

In this part, you will be asked to create a simple `.sql` seed migration,
which will create the basic database structure. We will then take this migration, run it and review what structure of the database have you chosen.

## What to focus on
- a clean, maintainable, and understandable design that supports the scenario.
- constraints that do not allow data inconsistencies
- indexes allowing the app to be performant
- using PostgreSQL dialect is appreciated

## What not to focus on
- inserting data

## Application scenario
_(Same for sql and api part)_

Our application should be a simple form editor.
Generally, we would like to see two use cases:
1. creating a form configuration with fields
2. filling out the form, which is based on the configuration.

### Configuring the form
There will be only one fixed form. I have to be able to add and delete fields.
Additionally, I can change the order of the fields.

Each field has one of two types. Either the field is textual or option selection.

Textual fields have a minimum and a maximum length. Select fields have multiple options, but at least two, one of which can be chosen.

All fields have their own label.

### Submitting the form
When configuration is ready, I should be able to list out all of the configured fields and send a form submission, which corresponds with this configuration. Also, I can display all of the form submissions along with the answers to the fields.