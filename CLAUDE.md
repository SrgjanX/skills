# Project instructions

## Before every commit: check for sensitive content

This repository is **public**. Anything committed can be seen by anyone, even if it is removed later.

Before each commit, review the staged changes (`git diff --cached`) and any new files for sensitive content, including:

- API keys, tokens, passwords, secrets or private keys
- `.env` files or other credential and config files with real values
- Personal data: email addresses, phone numbers, home addresses, ID numbers
- Real names, emails or details of clients, colleagues or companies used in examples
- Internal URLs, server names, IP addresses or file paths that reveal private information
- Confidential business information (prices, contracts, internal documents)

If anything sensitive is found, **stop the commit**. Tell the user what was found and in which file and line, and wait for their decision.

If nothing sensitive is found, go ahead with the commit.
