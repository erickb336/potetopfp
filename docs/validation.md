# Validation and limits

The launch checks combine automated tests, browser QA, and a small set of real AI requests.
The evidence below describes those checks. It does not promise identical results for every photo.

## Real portrait tests

The current recipe produced **six accepted portraits in seven live attempts**, across local, private hosted, and production environments.
Each attempt made one subject check, one image-generation request, and one quality check. No automatic regeneration ran.
One candidate failed the quality check and was not delivered or added to the showcase.

The five displayed examples come from these accepted results:

| Example | Test environment |
| --- | --- |
| Erick, with backpack | Production |
| Alexandr Wang | Private hosted staging |
| Tibo | Private hosted staging |
| Kanye | Private hosted staging |
| Zendaya, with dark curls | Local server using the live AI provider |

The remaining accepted test used a different Zendaya photo. Seven attempts are a small quality sample, not a reliability benchmark.

## Checked before the first production opening

- The automated suite covered job state, spending reservations, batch caps, input validation, and cleanup behavior.
- Two independent review cycles examined code, security, and user experience.
- A real production upload completed generation, quality review, and a PNG download.
- Reloading the same browser recovered the saved result.
- A different guest session could not retrieve that job or portrait.
- Public requests could not fetch source, environment files, databases, or private templates.
- Cross-origin submission was rejected, and the R2 bucket had no public access.
- The production metadata, canonical URL, robots file, and sitemap were checked.

The launch team retains the detailed records privately. Raw logs, job identifiers, and infrastructure identifiers are excluded from this repository.

## Soft-launch update

The final updated build passed **251 automated tests** with no failures or skipped tests.
The browser checks covered all five showcase cards, full-card expansion, keyboard dismissal, and navigation wraparound.
Responsive viewport checks at 320, 390, and 850 CSS pixels found no horizontal overflow.
The progress bar reads successful deliveries from the server and excludes queued reservations.
The deployed JavaScript, styles, and changed portraits matched the checked local assets.

## Limits

- The AI can still misrepresent a person's features or miss a quality problem.
- The provider invoice has not been reconciled against application accounting.
- The full 24-hour production expiry window has not been observed in real time.
- Stripe checkout opened correctly, but no real tip payment or payout was completed during QA.
- Browser checks do not replace testing every phone, camera, or assistive technology.

The free batch remains limited to 100 successful portraits, subject to the $40 application AI allowance.
Any later increase or new batch requires the owner's decision.
