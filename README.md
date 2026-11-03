# Harness by Heoka: connector

Harness is a business brain for small UK firms. It works with Xero and the mailbox, and gives your own Claude or ChatGPT a memory of your business: who owes you money, which quotes have gone quiet, and which emails are waiting on a reply. Nothing sends without a person. Harness drafts, you approve, and the send happens only on a human tap.

Price: 19 pounds a month for the whole company, with 7 days free.

This repository holds connection details only. There is no product code here.

## Connect

Connect URL (remote MCP server, streamable HTTP):

```
https://mcp.heoka.co.uk/mcp
```

- [Connect from Claude](clients/claude.md)
- [Connect from ChatGPT](clients/chatgpt.md)

## Sign-in (OAuth)

Sign in with your Harness account when your client asks. The server answers 401 to anonymous calls by design: a call without a signed-in Harness account is refused, and the 401 points your client at the OAuth sign-in. Each connection sees only your own company.

## Tools

Twelve tools. Reads take a `view`, writes take an `action`, and both take `args`.

| Tool | Kind | What it does |
|---|---|---|
| `today` | read | The overview: money, inbox, approvals, connections, the morning brief, to-dos |
| `inbox` | read | Mail and the people in it: who is waiting on a reply, threads, search, found bills and invoices |
| `person` | read | One customer or contact: relationship, timeline, statement, call brief, payment habit |
| `money` | read | Money from the books: cash, forecast, aged debtors, invoices, payments, chase plan |
| `workspace` | read | What Harness knows and has done: activity, memory, tone, connections, approvals |
| `draft` | write | Writes drafts for a human to approve; nothing sends from here |
| `approve` | write | Approves, skips or snoozes drafts; a send is staged and a human confirms it |
| `resolve` | write | Closes an open item: a to-do, promise, found invoice, bank match or call |
| `lists` | write | Who gets treated how: VIP, ignore, mute, never chase, suppress |
| `settings` | write | Changes one setting, such as tone or autonomy |
| `memory` | write | What Harness remembers: remember, forget, erase a correspondent's stored mail |
| `pay` | write | Payment links and captured leads |

The live list for your account comes from the server itself once you are connected.

## Trust

- Security: https://heoka.co.uk/security
- Trust: https://heoka.co.uk/trust
- Privacy: https://heoka.co.uk/privacy-policy
- Security reports: see [SECURITY.md](SECURITY.md)

## Support

connor@heoka.co.uk

---

All rights reserved, Heoka Partners Limited.
