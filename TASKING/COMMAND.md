
## User voice dictation command feeds/channels & history tracking
When a user inputs a command, primarily through voice, there might be long pauses, and corrections in what is fed into the command stream. With modifiers like "quote"/"Unquote" to provide context for what is said.
- Raw Voice to Speech text stream. (with raw non-verbal sound descriptions and pauses)
- Condensed command stream. (cleaned up with transcripted annotations)
- Formatted commands stream

Example: "Write down, uhm, the ehmm...... what's that thing called again? oh yeah a pedestal with a bucket. And then paint it black or somethings"
Raw: "Write down, uhm, the ehmm... {pause} what's that thing called again? {pause} Oh yeah a pedestal with a bucket. And then paint it black"
Condensed: "Write down 'a pedestal with a bucket'. Then Paint it black"
Formatted, something like: [
  {
    user: 0,
    action: 'write_down',
    text: 'a pedestal with a bucket'
  },
  {
    user: 0,
    action: 'paint',
    color: 'black'
  }
]