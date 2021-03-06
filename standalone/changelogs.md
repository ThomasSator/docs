# Changelogs
---
## Version 1.1.1 (September 14th, 2016)
- Improvement: `MySQLStorageDriver` is shipped with the package by default
- Improvement: Attachment now works with Intended Actions
- Improvement: Remove `$bot->run();` method on `public/index.php`
- Fix: `Driver Not Found` exception in strict mode

## Version 1.1 (August 30th, 2016)
- New: Add Attachment Handler
- New: Add MySQLStorageDriver and WordPressStorageDriver
- Improvement: Callback now takes up to 3 arguments: `$bot`, `$user_id`, and `$input`
- Improvement: Use `?subscribe` instead of `/subscribe.php`
- Fix: `$bot->say()` method doesn't works with two levels array generics and buttons
- Fix: Text Matching when `foo` works same as `%foo`

## Version 1.0.1 (August 13th, 2016)
- New: Quick Replies
- Improvement: Temporary remove Auto Stop feature since this makes people feel complicated
- Improvement: Add PHPUnit test suite
- Fix: Intended Actions loop or sending only 1 time.
- Fix: User can't set question mark in their pattern

## Version 1.0 (Jul 21st, 2016)
- Initial Release