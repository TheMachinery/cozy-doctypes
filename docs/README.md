Table of contents
=================

## Cozy doctypes

- [Accounts](io.cozy.accounts.md): Konnector accounts
- [Bank](io.cozy.bank.md): banking related data
- [Bills](io.cozy.bills.md): bills
- [Salaries](io.cozy.salaries.md): salaries
- [Contacts](io.cozy.contacts.md): instance owner contacts
- [Files](io.cozy.files.md): files documents
- [Konnectors](io.cozy.konnectors): Connectors
- [Notifications](io.cozy.notifications.md): notifications made by the apps
- [Photos Albums](io.cozy.photos.albums.md): photos albums
- [Remote requests](io.cozy.remote.requests.md): logs of requests via the remote doctypes
- [Sessions Logins](io.cozy.sessions.logins.md): sessions logins entry
- [Triggers](io.cozy.triggers.md): Job triggers

## Metadata

Every doctype should have `metadata` fields.

* `version` is be useful for migrations
* `dateImport` is useful for debugging purposes

```
{
  _id: '123456',
  metadata: {
    version: 1,
    dateImport: '2018-02-22T14:54:36.861Z'
  }
}
```

## Date format

Date should be formatted in [ISO8601](https://fr.wikipedia.org/wiki/ISO_8601) :
 
* `2017-04-22T01:00:00-05:00` ✅
* `2017-04-22T01:00:00Z` ✅
* `2017-04-22 01:00` ❌
