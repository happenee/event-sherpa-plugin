# Happenee for Claude and ChatGPT

Event Sherpa plans your events with you in Happenee, the Event Operations Platform, from the first brief to an event set up in Happenee.

This repository holds the published plugin package. Report problems through https://en.happenee.com/about/contact.

## What the plugin contains

The plugin carries eight Event Sherpa roles as skills:

- **Event Designer** turns your brief into an Event Story: the attendee's path through the event and what to set up for it.
- **Content Manager** drafts the agenda, speakers, partners and texts.
- **Registration Manager** plans the registration form and the attendee journey.
- **Communication Manager** plans the invitation, reminders and other e-mails.
- **Web Designer** plans the event microsite.
- **App Designer** plans the event app.
- **Event Insights** explains event results and comparisons.
- **Product Specialist** answers how Happenee works from the Help Center, with a link to the article.

The skills contain no executable code. They are instructions, reference files and Happenee Help Center articles that your AI assistant reads.

## Install in Claude Code

In Claude Code, add the Happenee catalog and install the plugin:

```
/plugin marketplace add happenee/event-sherpa-plugin
/plugin install happenee@happenee
```

Then run `/mcp`, sign in with your Happenee account and choose the events Claude Code may work with.

## What it connects to and where your data goes

The plugin connects your assistant to the Happenee server at `https://admin2.happenee.com/mcp/event-insights`. You sign in with your own Happenee account (OAuth). The assistant then sees only the events your account can access and only within the permissions you grant.

- Your conversation is processed by the AI provider you use (Anthropic for Claude, OpenAI for ChatGPT) under that provider's terms.
- When the assistant reads or prepares something in Happenee, the request and its data travel between the assistant and Happenee's server. Happenee processes them under its privacy policy.

What the assistant may do depends on the permissions your Happenee account has and the consent you give when connecting. It can read your events, agenda, registration, content and aggregate statistics. Where your workspace allows changes, private drafts within the scope you asked for are saved and read back, and publishing, opening registration, sending or scheduling e-mails, deleting and immediately visible changes wait for your explicit approval of the concrete preview and its effects. Feedback is sent only after you confirm it.

To revoke access immediately, open the connection manager in Happenee administration and disconnect. Disconnecting only in your AI assistant may leave the authorisation active until it expires after 7 days.

Event Sherpa is an AI assistant. Texts and proposals are prepared by AI, so check them before you save or approve them.

## Links

- Website: https://en.happenee.com/
- Privacy policy: https://en.happenee.com/about/privacy-policy#event-sherpa
- Terms of use: https://en.happenee.com/about/terms-of-use#event-sherpa
- Support: https://en.happenee.com/about/contact
