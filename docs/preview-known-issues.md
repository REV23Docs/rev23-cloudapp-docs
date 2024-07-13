# Known Issues (Release Preview)

Check this list for known issues, bugs, etc... during testing.

This list contains the following work items:

`BUG`: A known issue that we intend to fix before launch version.
`TBD`: A known limitation or missing feature. It is not determined if it will make it to launch version.
`TEST`: This item is completed and is currently being tested internally, it will be released to testers soon.
`WIP`: This item is in progress and will be in a test version before launch


### General

1.	There are instances where things have been implemented on web but are not on iOS and vice versa. Some things, such as the Template Designer are exclusive to web right now and will be for release, meaning you need to use the web app to customize your release forms. Other minor things we are in the stages of polishing up so things will align over the coming weeks.

### iPad

1. `BUG`: **AFTER UPDATING TO build 213.0** from a previous version you will likely experience a crash. Uninstall the app then reinstall from home screen if this occurs.
1. `TBD`: Complete Service button isn't currently doing anything. Evaluating its purpose based on feedback.
1. `WIP`: Needle config from settings menu. You can add needles from within a session, but edit/delete must occur on web for now
1. `TEST`: Merge customers
1. `TEST`: Implement newer avatars (colored initials circle) for consistency with all platforms

### Web

1. `BUG`: Occasionally creating a new user fails with a message indicating required fields are missing. Investigating.
1. `WIP`: Many polish items regarding layout, colors, sizing, etc...