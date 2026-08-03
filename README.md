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

> Our firms get calls in April from clients who owe a penalty nobody warned them about. The firm usually could have seen it coming months earlier — the information was sitting in last year's return the whole time. But nobody's going to check 400 clients by hand in September. Build us something that surfaces this across a firm's whole book and helps them actually do something about it.

That's the ask as we'd give it to you internally. Figuring out what it means is the project.

Some texture on how this plays out in a firm. The people who get hurt here are rarely the straightforward W-2 clients — they're the ones whose year didn't look like last year. The consultant who left a salaried job in March. The client who sold a rental property. The one whose spouse started a business. The firm's exposure isn't uniform either: some of these clients are a phone call and a fixed problem, some are a phone call and an apology, and telling those apart in September is worth a great deal more than telling them apart in April.

There's also a question of what the firm does with the answer. Identifying a problem the firm can't act on isn't worth much. And whatever leaves the firm's hands and reaches a client is something the firm is professionally responsible for.

In `/data` you'll find client records for a fictional CPA firm — prior-year return summaries and current-year activity to date. The records are deliberately heterogeneous, and the variation is part of the specification. Read the data before you write code; some of the requirements are in there rather than here.

**The bar is that a CPA could put the output of this in front of a real client.**

That has two edges. The first is correctness: the calculations here are governed by specific rules, and those rules have exceptions, thresholds, and timing quirks that determine the answer for exactly the clients this product exists to catch. Getting the typical client right is not difficult and is not what we're evaluating. The awkward ones are the entire point, and a tool that's confidently wrong about them is worse than no tool at all.

The second is what the firm is allowed to do. Accountants operate under real constraints on how they advise clients, what they do with client information, and what has to happen before something goes out the door. We're not going to enumerate those constraints for you. Finding them, judging which ones bear on this product, and designing around them is a substantial part of what we're looking at — and it's the part most engineers building for this industry get wrong.

Assume tax year **2025** throughout.

## Scope

You generally shouldn't spend significant time on: auth, multi-tenancy, deployment, test coverage, real email delivery, state-level tax, or integration with any payment system. These will not be evaluated as part of this project and should exist to the extent that's needed to make the app functional. Feel free to stub anything requiring a third party.

You may use any stack you like.

Where this project brief is ambiguous, make a decision and document the assumption. We'd rather see a decisive interpretation you can defend than a hedge that covers everything shallowly. Scoping is a big part of this job. A clearly reasoned omission is better than a shaky implementation.

## What To Submit

Assign @seanmcoleman read access to a new GitHub repository containing all code with whatever instructions we need to start it. Assume we have a normal dev environment and nothing else. 

A link to a live, hosted demo environment that we can share with our CPA team to test.

**A short write-up** — drop it in a new file and answer these:

- What did you build?
- What did you deliberately leave out, and why?
- What would you have asked us, if you could have?
- What are you unsure about?

One page is plenty. Bullets are fine. We read this closely — it's the closest thing in this process to how you'd actually communicate with us day to day.

## On AI Tools

Use whatever you'd use on the job, including AI since that's how we work. But note the live session above: anything you ship, you own and will be editing in front of us. Fair warning on this domain specifically. Models are confident and fluent about tax rules and frequently wrong in ways that read fine. The failure mode is a clean implementation of a rule that doesn't exist. Verify things.

## Housekeeping

You own what you build. We're licensing it for evaluation only and won't use it in our product.

Please don't publish the brief or the dataset. It isn't fair to the people going through this after you.
