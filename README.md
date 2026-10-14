# CREparser Lease Abstraction for Claude

CREparser Lease Abstraction turns a commercial real estate lease PDF into a
reviewable abstract. Claude reads the whole lease, including any amendments, and
drafts key terms, the base rent schedule, critical dates and risk flags. CREparser
finds every quoted clause in the PDF. A viewer then opens in the conversation, where
each term links to its highlighted clause, notice deadlines sit on a term timeline,
and you can approve or flag each term. Export a PDF abstract, a spreadsheet, the
highlighted lease or a calendar of critical dates.

This plugin connects Claude to the CREparser service at
`https://mcp.creparser.com/leases/mcp`. It also adds a skill that guides Claude
through reading, validating and showing an abstract. It works in Claude chat, Cowork
and Claude Code.

## Try it

Watch the [demo video](https://www.youtube.com/watch?v=W9lC6Lx4Ljk).

Attach a lease and ask, for example:

- "Abstract this lease."
- "When do I need to give notice to renew or terminate this lease? Show me the clauses."
- "Compare the rent, expiration and risk flags across these leases."

To try it without a real lease, use the fictional
[sample office lease](https://mcp.creparser.com/samples/sample-office-lease.pdf).

## Sign in

The first time Claude uses CREparser, it asks you to connect your CREparser account.
Sign in with Google, and a free account is created automatically. Free accounts can
import 5 documents. For more, email
[creparser@superdocs.io](mailto:creparser@superdocs.io).

In Claude chat and Cowork, Claude sends your attachment to CREparser from its code
sandbox. To allow this, add `mcp.creparser.com` under **Settings → Capabilities →
Code execution and file creation → Network access**. If you don't, Claude offers a
picker where you select the PDF yourself.

## Your data

- CREparser receives only the PDFs you attach or select. It reads their text to find
  the quoted clauses. Your leases are private to your account.
- Leases, the text read from them, and your abstracts are deleted automatically 24
  hours after you last use them. You can ask Claude to delete a lease from CREparser
  at any time.
- For your account, CREparser keeps a scrambled account identifier, your plan and how
  many documents you have imported, so it can apply your plan's limits. Your email
  address and login details stay with the sign-in service.
- CREparser checks where each quotation appears in the lease. The abstract is Claude's
  reading of the lease. It is not legal advice.

See the [privacy policy](https://www.creparser.com/privacy) and
[terms of service](https://www.creparser.com/terms).

## Install in Claude Code

```sh
claude plugin marketplace add superdocsio/creparser-leases-claude-plugin
claude plugin install creparser-leases@creparser
```

## Support

Email [creparser@superdocs.io](mailto:creparser@superdocs.io), or see
[creparser.com](https://www.creparser.com). CREparser is made by Superdocs.
