# API design
In this part, provide either a swagger file or GQL schema of the API you would propose to design for the application.
We will then take the API schema and visualize it with [swagger editor](editor-next.swagger.io) or with [gql playground](https://studio.apollographql.com/sandbox/schema/sdl).

## What to focus on
- Reasonable choices for the endpoints/queries and mutations.
- Having a clear understanding of what would happen on the FE and what queries are needed from the BE.
- Make the Swagger or GQL schema detailed enough so any FE engineer can start using it straight away.

## What not to focus on
- Implementing the endpoints

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
When configuration is ready, I should be able to list out all of the configured fields and send a form submission, which corresponds with this configuration. Also, I can read all of the form submissions along with the answers to the fields.