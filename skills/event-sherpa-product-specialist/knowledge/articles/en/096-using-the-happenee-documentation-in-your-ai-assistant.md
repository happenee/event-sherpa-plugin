# Using the Happenee documentation in your AI assistant

> How to give ChatGPT, Claude, or another AI assistant access to the current Happenee documentation: an instruction to copy and what to watch out for.

- Article in the Help Center: https://help.happenee.com/en/articles/96-using-the-happenee-documentation-in-your-ai-assistant
- Česká verze: https://help.happenee.com/cs/articles/96-dokumentace-happenee-ve-vasem-ai-asistentovi
- Collection: Event Sherpa
- Updated: 2026-09-01

---

> [!info] Overview
> If you plan your event in ChatGPT, Claude, or another AI assistant, you can give it access to the current Happenee documentation. Paste a short instruction from this article into your project — the assistant will then load the relevant help articles whenever a question concerns Happenee and combine them with what it knows about your event. For quick questions while you work in the admin, Event Sherpa is the shortest path; your own AI assistant suits planning in the broader context of your event. There is nothing to install; the instruction works in any AI tool that can read web pages.

## Getting started

- Open the AI tool where you plan your event — typically a ChatGPT or Claude project that already holds your brief, agenda, or budget.
- Paste the instruction from the Details section into your project instructions (in ChatGPT and Claude you'll find them in the project settings; in other tools, use the system instructions).
- Make sure the assistant is allowed to read web pages. Without web access, the instruction cannot work.
- Ask a test question — for example, "How do I set up registration for VIPs and regular guests in Happenee?" — and check that the answer links to articles from help.happenee.com.

## Details

### Event Sherpa or your own AI assistant?

Event Sherpa is the AI assistant directly in the Happenee admin. It knows this documentation, sits right next to the setting you are working on, and answers questions like "how do I set up registration" or "where do I find exports" immediately — it guides you through the steps, while you make the changes in the admin yourself. Your own AI assistant adds a second perspective: it knows the context of your event, which makes it useful for planning and decisions.

- **Event Sherpa** — questions while you work in the admin: how to set something up, where to find it, why something behaves differently than you expect. It answers immediately, with no preparation.
- **Your own AI assistant** — planning and decisions in the context of the whole event: it combines the Happenee documentation with your brief, agenda, and budget.

Both draw on the same documentation, so their answers don't contradict each other — choose based on where you are working right now.

### Instruction to copy

Copy the entire contents of the box (all seven points, including the addresses) and paste them into your AI project instructions:

```
1. Whenever the conversation concerns Happenee (event setup, registration, microsite, e-mails, agenda, check-in, reporting), do not answer from memory. The documentation at help.happenee.com changes continuously, and your internal knowledge may be outdated. If they conflict, the loaded content wins.
2. Based on the topic, load the collection page with the list of articles:
   - Getting started with Happenee: https://help.happenee.com/en/collections/1-getting-started-with-happenee
   - Event setup and registration: https://help.happenee.com/en/collections/4-event-setup-and-registration
   - Content and attendee experience (microsite, agenda, apps): https://help.happenee.com/en/collections/9-content-and-attendee-experience
   - Communication and invitations (e-mails, campaigns): https://help.happenee.com/en/collections/13-communication-and-invitations
   - Event day and on-site operations (check-in): https://help.happenee.com/en/collections/17-event-day-and-on-site-operations
   - Reporting and post-event work: https://help.happenee.com/en/collections/20-reporting-and-post-event-work
   - Event Sherpa (recommended setups by event type): https://help.happenee.com/en/collections/23-event-sherpa
   - Troubleshooting: https://help.happenee.com/en/collections/27-troubleshooting
3. Pick one to three relevant articles from the list and load them in full. Only then answer.
4. Build the answer on two sources: take Happenee facts exclusively from the loaded articles, and event specifics (target groups, agenda, budget) from the context of this project.
5. Include the full addresses of the articles you used, so the organizer can open them.
6. When the documentation does not cover a topic, say so explicitly and suggest asking Event Sherpa directly in the Happenee admin. Never describe features that are not in the loaded documentation.
7. If you cannot load web pages, say so and mark the answer as potentially outdated.
```

### How the instruction works

The instruction takes the assistant down the same path you would take in the help center yourself: first the list of articles in a collection, then one to three specific articles, and only then the answer. The point is staying current — the documentation changes with the product, while AI models remember the state as of their training date. An assistant that loads the articles works with exact terms, current steps, and warnings about common mistakes, and it can apply all of that to the specific event you are planning with it.

## Common pitfalls

### An assistant without web access answers from memory

If web browsing is turned off in your AI tool, the instruction has no way to work, and the assistant answers from its training data — which can be many months old. You can tell by the missing links to help.happenee.com in the answer.

### Loading the documentation is not guaranteed every time

Even with the instruction in place, the model may occasionally answer straight from memory. If an answer doesn't look current or doesn't link to the help center, ask: "Verify this in the Happenee documentation." The assistant loads the articles and corrects or confirms the answer.

### The assistant cannot see into your admin

The documentation describes how Happenee works — the assistant cannot learn the state of your event, the number of registered attendees, or the contents of your admin from it. You'll find the answer to questions like "how many people have registered so far" in the event admin, not in the documentation.

### Attendee personal data doesn't belong in an external AI

The assistant doesn't need any personal data to work with the documentation. Don't paste names, e-mail addresses, or registration exports into an external AI tool — sharing them with a third party falls under your GDPR obligations.

## Related articles

- [What is a workspace and what is an event](https://help.happenee.com/en/articles/1-what-is-a-workspace-and-what-is-an-event)
- [Recommended order for setting up an event step by step](https://help.happenee.com/en/articles/8-recommended-order-for-setting-up-an-event-step-by-step)
