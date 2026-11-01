> “There is nothing more powerful than an idea whose time has come.”
>
> — Victor Hugo

# What if money could follow an instruction?

A check is a familiar idea: it carries an instruction to settle an obligation. Behind that piece of paper is a process for checking authority, applying rules, moving value through financial institutions, and keeping a record.

What if that process could be programmable—and adapt to the financial services people already use?

## A Settlement Operating System

An operating system provides shared capabilities on which different applications can be built. **x-change applies that idea to settlement.** It provides a foundation for issuing and processing governed financial instructions, so institutions can build their own applications around them.

A Pay Code represents an instruction. Behind it, x-change coordinates the work: validation, authorization, routing, execution, and evidence. Provider integrations connect to supported financial services; separate packages handle responsibilities such as instructions, claim workflows, treasury positions, and journals.

The distinction matters: a Pay Code does not itself hold money or move it. Financial execution depends on the relevant authority, provider, and evidence.

[x-change](https://github.com/3neti/x-change) is a public beta. It is my attempt to make this idea practical for banks and other financial institutions that want to build and operate their own platforms.

**Money should adapt to people. Not the other way around.**

## See it in action

[x-PayOut](https://payout.disburse.cash) is an application powered by x-change. Its home page includes a safe walkthrough: draft an instruction, issue a Pay Code, and let the recipient claim a payout to a supported bank or wallet.

## Build your own

Start with a new Laravel application and install x-change as a package:

```bash
laravel new x-PayOut
cd x-PayOut
composer config minimum-stability beta
composer config prefer-stable true
composer require '3neti/x-change:^1.0@beta' -W
php artisan x-change:setup
```

These commands start a local evaluation. Commissioning an institution's platform also requires its own provider configuration, infrastructure, operational controls, and acceptance. See the [getting-started guide](https://github.com/3neti/x-change/blob/main/GETTING_STARTED.md).

I have extracted and refactored domains into focused packages so future developers can understand, extend, and work on different parts independently.

## Explore, question, or license it

I welcome developers, banks, financial institutions, and independent reviewers to try the experience, examine the work, and discuss where the idea could go.

[Try x-PayOut](https://payout.disburse.cash) · [Explore x-change](https://github.com/3neti/x-change) · [Discuss licensing](https://3neti.com/contact-us)

— LB Hurtado, software artisan
