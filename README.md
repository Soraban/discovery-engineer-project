# Discovery Engineer — Build Project

This project is built to look like the actual job: a loose problem, incomplete requirements, an unfamiliar domain, and a short runway.

## About Soraban

Soraban builds workflow automation for CPA firms. We're a Series A company selling into an industry that runs on email attachments, PDF checklists, and a shared drive nobody has reorganized since 2019.

Our customers are accounting firms ranging from a handful of preparers to a few hundred. A mid-sized firm might carry a couple thousand clients — individuals, partnerships, S corps, trusts — and the ratio of clients to staff is brutal. During filing season the firm is running hundreds of returns in parallel, each blocked on something different, and the person holding that state is usually a preparer with a spreadsheet and a good memory.

A few things about the industry that shape everything we build: It is extraordinarily seasonal — most of the year's revenue lands in about ten weeks, and a product that isn't ready by January is a product that waits a year. It is trust-heavy: firms carry professional liability for their work and are regulated in how they handle client data and what they can say to clients, so software that ignores those constraints doesn't get adopted no matter how good it looks. And CPAs are extremely good at spotting software built by people who've never done the work. Every product decision we make gets validated against practitioners, including this project. Real CPAs will review what you build.

## The Role

The Discovery Engineer role works directly with our CEO and Head of Product on problems that arrive as a brief statement and a hunch. Your job is to turn that into specific functionality and build it far enough that we can put it in front of a firm and learn something.

That means most of the work is upstream of code: deciding what the thing actually is, what it must get right, what can wait. Then building it quickly and well enough that a practitioner takes it seriously. You'd be learning a dense, unfamiliar domain continuously and getting to competent fast — not expert, but competent enough to make good calls without a CPA in the room.

This project is a small version of that.

## The Problem

> Firms get calls in April (before the filing deadline) from clients who owe an underpayment penalty nobody warned them about and are frustrated. The firms usually could have seen it coming months earlier in the prior year since they have those prior year returns. But nobody's going to check hundreds of clients by hand before the end of the tax year to help clients avoid penalties. Build us something that surfaces clients who are at risk of penalties for the current tax year (2025), across a firm's whole book.

Some texture on how this plays out in a firm. The people who get hurt and pay penalties here are rarely the straightforward W-2 clients — they're the ones whose year didn't look like last year. The consultant who left a salaried job in March. The client who sold a rental property. The one whose spouse started a business. The firm's exposure isn't uniform either: some of these clients are a phone call and a fixed problem, some are a phone call and an apology, and telling those apart before the tax year ends is worth a great deal more than telling them apart in April.

Assume we are currently in tax year **2025** (i.e. today is September 2025) and we are looking back on the prior **2024** tax year (for which returns were filed). In `/data` you'll find client records for a fictional CPA firm — prior-year (2024) return summaries and current-year (2025) activity (payments, withholdings, etc) to date. The records are deliberately heterogeneous.

Build a dashboard showing a list of clients and information about potential under/over payments that could result in penalties for tax year 2025. Since we are assuming that we're in 2025, with this dashboard, firms can contact clients who are on track to owe a penalty and inform them — before the year is over. With this, clients can make additional tax payments to avoid penalties when ultimately filing their 2025 return. 

## Scope

You generally shouldn't spend significant time on: auth, multi-tenancy, deployment, test coverage, real email delivery, state-level tax, or integration with any payment system. These will not be evaluated as part of this project and should exist to the extent that's needed to make the app functional. Feel free to stub anything requiring a third party.

You may use any stack you like.

Where this project brief is ambiguous, feel free to ask questions or make a decision and document the assumption. We'd rather see a decisive interpretation you can defend than a hedge that covers everything shallowly. Scoping is a big part of this job. A clearly reasoned omission is better than a shaky implementation.

## What To Submit

Assign @seanmcoleman read access to a new GitHub repository containing all code with whatever instructions we need to start it. Assume we have a normal dev environment and nothing else.

## On AI Tools

Use whatever you'd use on the job, including AI since that's how we work.
