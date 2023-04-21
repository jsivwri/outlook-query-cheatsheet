# Outlook Raw Query Search Cheatsheet

Microsoft Outlook for Mac allows you to perform advanced searches with raw queries. This cheatsheet outlines key query parameters and examples to help refine your searches in Outlook for Mac (latest version).

## Query Parameters

| Query Parameter      | Description               | Example                   |
| -------------------- |---------------------------|---------------------------|
| `from:`              | Search messages from a specific sender | `from:john@example.com` |
| `to:`                | Search messages sent to a specific recipient | `to:jane@example.com` |
| `cc:`                | Search messages with a specific recipient in the carbon copy (cc) field | `cc:jim@example.com` |
| `subject:`           | Search for words in the subject line | `subject:Important` |
| `attachment:`        | Search for messages with attachments | `attachment:invoice` |
| `category:`          | Search for messages with a specific category | `category:red` |
| `read:`              | Search for messages marked as read or unread | `read:false` |
| `flagged:`           | Search for messages flagged for follow up | `flagged:true` |
| `DATEFIELD:>=DATE`   | Search messages within a specific date range | `received:>=2022-01-01` |

*Note: Replace `DATEFIELD` with `received`, `sent`, or `due` to search within received, sent, or due messages respectively. Replace `DATE` with a specific date (YYYY-MM-DD).*

## Examples

### Searching for a specific word or phrase

To search for a specific word or phrase (case insensitive), simply type the word or phrase:

```
example
"example text"
```

### Combining search parameters

Use a combination of search parameters to refine your search. Separate each parameter with a space:

```
from:john@example.com "meeting minutes"
to:jane@example.com subject:Important
```

### Searching for messages within a specific time frame

Search for messages received in a specific time frame:

```
received:>=2022-01-01 received:<=2022-01-31
```

### Using Boolean operators

Combine search parameters with Boolean operators (`AND`, `OR`, `NOT`):

```
subject:Annual AND subject:Report
from:john@example.com OR from:jane@example.com
subject:Invoice NOT from:john@example.com
```

Remember to capitalize Boolean operators.

## Additional Query Parameters

| Query Parameter      | Description               | Example                   |
| -------------------- |---------------------------|---------------------------|
| `body:`              | Search for specific words in the message body | `body:Goals` |
| `size:`              | Search messages by size (B: Bytes, KB: Kilobytes, MB: Megabytes) | `size:>5MB` |
| `priority:`          | Search messages with a specific priority (high, normal, or low) | `priority:high` |

## Advanced Usage

### Phrase Searches

```
"Vacation plan"
"Project proposal"
```

### Wildcards

```
Budget*.xls
daily-rep?rt.pdf
```

### Proximity Searches

Search for terms within a specific distance (where `n` is the number of words) from each other with the `NEAR` operator:

```
"Budget report" NEAR3 Summary
```

### Grouping

Use parentheses to group search criteria:

```
(subject:annual OR subject:quarterly) AND subject:report
```

## Additional Examples

### Search for high-priority emails with attachments

```
priority:high attachment:*
```

### Search for messages with a specific word in the subject and body

```
subject:project body:update
```

### Search for messages containing specific file types

```
attachment:*.pdf
attachment:*.pptx
```

### Search for messages excluding specific categories

```
NOT category:blue
```

### Search for messages with specific words in the body and a size range

```
body:contract size:500KB..1MB
```

With this extended cheatsheet, you should be able to efficiently perform raw query searches in Microsoft Outlook for Mac (latest version). Remember that you can mix and match various query parameters and operators to create specific searches tailored to your needs.
