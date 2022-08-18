# Error

Most Google APIs use resource-oriented API design. Instead of
defining different NOT_FOUND errors, the server uses one standard
NOT_FOUND code, and tells the client which specific resource was not
found.

The smaller error space has advantages:

- reduces the complexity of documentation
- affords better idiomatic mappings
- reduces client logic complexity, without restricting inclusion of
  actionable information

## Model

```ts
type Error = {
  code: number
  message: string
  details: any[]
}
```

- `Error.code`: simple code, easily handled by client
- `Error.message`: Developer-facing human-readable error
- `Error.details`: Additional error information for client
  - retry info
  - help link, etc.

## Code

- Individual APIs __must__ avoid defining additional error codes.
- Developers must use canonical error codes.
- Handling an average of 3 error codes per API call would mean most
  application logic would just be for error-handling.

## Message

Error messages should help users understand & resolve API errors
easily.

- Do not assume the user to an expert user of the API.
- Do not assume user knows anything about service implementation.
- Should be constructed such that technical users can respond, and
    correct it.
- Keep the message brief. If needed, provide a link to more info,
    questions, feedback. Otherwise, use "details" field.

## Details

|  |  |
|--|--|
| information | 1xx |
| successful  | 2xx |
| redirection  | 3xx |
| client error | 4xx |
| server error  | 5xx |
