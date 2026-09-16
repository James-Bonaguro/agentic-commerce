# Ecommerce & Site Audit Checklist

The step that happens before [`audit/`](../audit/README.md). That folder measures what
assistants say about a business. This measures the business itself — the site, the
social presence, and the retail reality — so the assistant-visibility findings land
on solid ground instead of guesses.

Built from a real run on a Chicago family pasta sauce brand relaunching direct-to-consumer.
Same honesty rules as [`audit/README.md`](../audit/README.md) apply here: quote the exact
page or URL for every finding, separate what you observed from what you're inferring,
and never state a number you didn't personally see in a tool result.

## 0. Setup
- Brand/site URL, social handles, and the stated goal for the call.
- Any recent change worth knowing before you start (rebrand, new integration signed,
  funding, relaunch).

## 1. Full site crawl
- Pull `sitemap.xml` first. It tells you the real page count before you trust the nav —
  note any mismatch between what's linked in nav/footer and what's actually indexed.
- Visit every top-nav and footer link. Flag orphaned pages (in the sitemap, not in nav)
  and dead nav links (in nav, 404 or redirect).
- Per product: name, price, size/unit, stock status, and the exact description text —
  and whether a real add-to-cart/checkout path is reachable, not just visible.
- Check explicitly for bundles, subscriptions, and merch — don't assume absence means
  none exist. Merch in particular tends to live only on social (see Section 2).
- Identify the platform from the page source (`<!-- This is Squarespace. -->`,
  `cdn.shopify.com`, WooCommerce classes) instead of guessing from the design.
- Shipping cost, free-shipping threshold, delivery promise, email/SMS capture incentive —
  quote exactly, or note "not stated anywhere."
- Reviews on product pages, store locator, footer copyright year, footer link-text-vs-href
  mismatches, mobile viewport check, rough load time.

## 2. Social audit
- Try the no-login surface before concluding "can't access." Instagram's profile root
  usually force-redirects to a login wall, but `instagram.com/<handle>/embed/` and
  individual `/p/` or `/reel/` URLs often render without one — enough to get follower
  count, post count, and real captions with dates.
- List actual post dates observed, not an estimated cadence.
- Quote what captions push toward — buying online, an in-person event, or nothing
  actionable.
- Flag anything mentioned on social that's absent from the website. This gap is usually
  the highest-value finding in the whole social section.

## 3. Retail/distribution reality check
Do this even when nobody asked about retail — it's where the biggest finding tends to
hide.
- Search the brand + category + major retailer names, even with no store locator on the
  site.
- Compare the retail listing price to the site's direct price for the identical SKU. A
  DTC price *above* retail, unexplained, is a real and quotable problem.
- Compare product names/descriptions across the site and retail listings. Mismatches
  confuse customers and are exactly what breaks assistant accuracy in Section 4.
- Check historical press and company pages (LinkedIn, etc.) for checkable claims
  (certifications, founding dates, past distribution) that don't appear on the current
  site — verify before repeating them as fact.

## 4. Assistant visibility — quick pilot, or the real thing
Full protocol: [`audit/README.md`](../audit/README.md) and
[`audit/query-sets.md`](../audit/query-sets.md) — 30 questions, 7 types, an afternoon.
When there isn't time before a call, run a smaller pilot and label it as one:
- ChatGPT (chatgpt.com) and Google AI Mode (`google.com/search?q=...&udm=50`) both work
  logged out. ChatGPT nudges toward sign-up after a handful of anonymous messages in the
  same session — expect that, and start a fresh chat per question regardless.
- Perplexity, Claude, and Gemini's conversational surfaces have required a logged-in
  account in testing — don't fake a workaround. A raw search-index check is not the same
  instrument as a synthesized assistant answer; if you use one, label it as supplementary,
  not as an assistant result.
- The single highest-value question is the bare-category one ("who's the best {category}
  in {city}") with **no brand name in it**. If the business doesn't appear and named
  competitors do, that is the finding — quote the competitors verbatim, don't extrapolate
  a percentage from one question.
- Two assistants can disagree about the same real-world fact (e.g., one says "yes, in
  stock" citing a third-party reseller while the other says "no, not directly, not
  verified") — when that happens, it's a finding in itself: whoever asks gets a different
  answer depending on which assistant they open first.

### Why a "small" inconsistency can cost more with an agent than with a person
A human skims past two slightly different descriptions of the same product and assumes
they're the same jar. An assistant assembling an answer from multiple sources doesn't get
that benefit of the doubt automatically — it may list both descriptions as if they were
different products, latch onto whichever source it found first and miss the rest of the
lineup, or invent a detail to fill the gap. In one real run, a single flavor-name mismatch
between a brand's own site and a retailer's listing was enough for one assistant to return
a nearly complete flavor list and another to return one flavor plus a garbled, made-up
name found nowhere in the source material. The fix (pick one description, use it
everywhere) is small. What it was silently costing wasn't.

## 5. Punch list
- 5-10 items, each a one-sentence fix, not a project.
- At least one item the client can do same-day.
- Never "rebuild the site" or "redo the brand" as a line item — that's a different
  conversation, and it's not what a punch list is for.

## 6. Owner questions
- Every place a finding depends on something you can't verify from outside (inventory
  status, whether a claim is current, what's actually behind a login wall).
- Phrase each as a specific, answerable question, not "tell me about your business."

## 7. Value framing — say this part out loud on the call
Keep this consistent with `audit/README.md`'s honesty rules: don't claim agent-driven
revenue matters today, because it doesn't yet. The honest pitch has two halves:
- **Today:** the fixes that help an assistant describe the brand accurately — consistent
  naming, real stock status, a working price — are the same fixes that help normal search,
  delivery-app listings, and a confused human customer. That value lands now, with or
  without agents.
- **Tomorrow:** whichever brand in a category is the easiest to describe accurately is the
  one still standing when assistants start actually transacting. Right now that's often
  decided by default, not by merit — a business can lose a category slot to a competitor
  for no better reason than having thinner, less consistent public data. That's a cheap,
  fixable gap today. It gets more expensive to close the longer it's ignored.

## 8. Call battle card (build last, from everything above)
One page. Top 5 facts in the order to say them, 3-4 likely objections with a one-line
response each, and the single concrete ask you want out of the call.
