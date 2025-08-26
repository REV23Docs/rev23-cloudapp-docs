# Flags

Flags are a list of attributes you can add to a customer to easily record past behavior to alert you about a potential problematic encounter, or to simply not book that person agian.

All a Flag object needs is a **Name**. You can configure this list as needed.

## Categorization

Flags optionally allow for using the `:` character as a separator for using categories. For example, you can use `Behavior: Anger Issues` and `Behavior: Disrespectful`. The user interface will then group these together.

```text
Behavoir
└─ Anger Issues
└─ Disrespectful
```

Categories are not required, but are recommended to help with organization if you have a large number of flags.

## Security

The permissions for creating/editing these objects are controlled by the `Customer Config` permission set.
