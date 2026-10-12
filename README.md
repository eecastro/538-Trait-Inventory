# Big Five Personality Inventory

A 30-statement Big Five personality inventory for classroom use, delivered as a single self-contained HTML file. Students rate themselves on 30 statements and receive percentile estimates for five broad traits and fifteen facets, plus research-based interpretation of how their traits combine.

**Take the inventory:** [https://eecastro.github.io/538-Trait-inventory/]
**Maintained by:** Eric E Castro, Psychology Dept, St Ignatius College Prep, San Francisco.

> This is an independent, unofficial teaching tool. It is not affiliated with or endorsed by FiveThirtyEight, ABC News, Christopher J. Soto, Oliver P. John, or the Colby College or UC Berkeley personality labs.

---

## Origins

### The FiveThirtyEight quiz

In 2018, FiveThirtyEight science writer Maggie Koerth-Baker published "Most Personality Quizzes Are Junk Science. I Found One That Isn't," part of the site's science-resolutions series. The article contrasted popular online personality quizzes with the Big Five model that most personality psychologists use, and it featured the work of Christopher J. Soto of Colby College.

In January 2019, Koerth-Baker and Julia Wolfe followed up with an interactive quiz, "Most Personality Quizzes Are Junk Science. Take One That Isn't." Built on Soto's research, it scored respondents from 0 to 100 on extraversion, agreeableness, conscientiousness, negative emotionality, and openness to experience; broke each trait into three subtraits; compared each person's results with the average American; and let users invite friends and family to compare profiles. Its 30 statements and three facets per trait match the format of the BFI-2-S, and education resources have listed the quiz as an authorized online version of the BFI-2.

### The underlying instrument: the BFI-2

The Big Five Inventory–2 (BFI-2) was developed by Christopher J. Soto (Colby College) and Oliver P. John (University of California, Berkeley) as a major revision of John's original Big Five Inventory. It measures five domains (Extraversion, Agreeableness, Conscientiousness, Negative Emotionality, and Open-Mindedness), each divided into three facets, for 15 facets in all. The full BFI-2 has 60 items. The BFI-2-S is a 30-item short form and the BFI-2-XS a 15-item extra-short form. All versions balance positively and negatively worded items to control for the tendency to agree with everything.

BFI-2 items are copyright 2015 by Oliver P. John and Christopher J. Soto.

### Why this reconstruction exists

In March 2025, ABC News shut down FiveThirtyEight as part of a round of layoffs and took the site offline, and the personality quiz disappeared with it. This project recreates the experience it offered (a short, research-grounded Big Five inventory with facet scores and interpretation of trait combinations) as a standalone page that instructors can host and control themselves.

---

## How this version relates to the original

This project reconstructs the *format* of the FiveThirtyEight quiz. It does not copy it.

- **The facet structure comes from the BFI-2.** The 15 facet names (Sociability, Assertiveness, Energy Level, Compassion, Respectfulness, Trust, Organization, Productiveness, Responsibility, Anxiety, Depression, Emotional Volatility, Intellectual Curiosity, Aesthetic Sensitivity, and Creative Imagination) and their grouping under the five domains are Soto and John's.
- **The statements come from the IPIP, not the BFI-2.** The 30 items were drawn from or adapted from the International Personality Item Pool (Goldberg et al., 2006), which is in the public domain. Each facet has two items, one worded in each direction, mirroring the design of the BFI-2-S.
- **Domain labels are the traditional ones.** This version uses *Openness* and *Neuroticism*; the BFI-2 calls these *Open-Mindedness* and *Negative Emotionality*.
- **No FiveThirtyEight material is used.** None of FiveThirtyEight's code, text, graphics, or data appears in this project. All interpretive text was written for this project.
- **Percentiles use approximate norms.** They are not FiveThirtyEight's comparison data or official BFI-2 norms (the BFI-2 authors note that there is no official manual with published norms).
- **This item set has not been validated as a unit.** Treat results as a learning and self-reflection tool, not as research-grade measurement.

---

## Credits

| Contribution | Credit |
|---|---|
| Big Five Inventory–2, its 15-facet structure, and facet names | Christopher J. Soto & Oliver P. John (Soto & John, 2017a, 2017b) |
| The FiveThirtyEight article and quiz that inspired this project | Maggie Koerth-Baker (2018); Maggie Koerth-Baker & Julia Wolfe (2019), FiveThirtyEight |
| The 30 inventory statements | International Personality Item Pool, [ipip.ori.org](https://ipip.ori.org) (Goldberg et al., 2006) |
| Reading two traits together ("personality styles") | Costa & Piedmont (2003) |
| Resilient, overcontrolled, and undercontrolled personality types | Robins et al. (1996); Asendorpf et al. (2001) |
| Research findings summarized in the feedback | See [References](#references) |
| Page design, code, and interpretive text | Drafted with Claude (Anthropic); reviewed and adapted by [Your Name] |

---

## Using the official BFI-2-S instead

If you would rather administer Soto and John's own items, the page is built to make that swap straightforward: replace the 30 statements in the `ITEMS` array near the bottom of `index.html`, keeping two items per facet and setting `key: -1` for reverse-scored items. Facet codes are:

| Domain | Facet codes |
|---|---|
| Openness | `int` Intellectual Curiosity, `aes` Aesthetic Sensitivity, `cre` Creative Imagination |
| Conscientiousness | `org` Organization, `pro` Productiveness, `rsp` Responsibility |
| Extraversion | `soc` Sociability, `ass` Assertiveness, `ene` Energy Level |
| Agreeableness | `com` Compassion, `res` Respectfulness, `tru` Trust |
| Neuroticism | `anx` Anxiety, `dep` Depression, `vol` Emotional Volatility |

Before you do, check the authors' current terms. The [Colby Personality Lab's BFI-2 page](https://www.colby.edu/academics/departments-and-programs/psychology/research-opportunities/personality-lab/the-bfi-2/) grants permission for personal and research use, and the [Berkeley Personality Lab](https://ocf.berkeley.edu/~johnlab/bfi.html) describes the BFI-2 as free for non-commercial research and directs commercial requests to the lab. Neither statement mentions classroom use specifically, so if you plan to post the official items on a public website, it is worth confirming with the authors. Keep the copyright notice with the items and cite both Soto and John (2017) papers.

---

## Using it in your course

**Hosting on GitHub Pages**

1. Put `index.html` and this `README.md` in a public repository.
2. Go to **Settings → Pages**, set the source to *Deploy from a branch*, choose `main` and `/ (root)`, and save.
3. After a minute or two the inventory is live at `https://<your-username>.github.io/<repository-name>/`.

**Previewing results.** Add `#demo` to the end of the URL to see a results page generated from random answers.

**Collecting results.** Students can print or save their results as a PDF, or download a one-row CSV containing trait and facet scores, percentiles, and raw item responses. Every CSV has the same columns, so they can be stacked into a single spreadsheet.

**Privacy.** All scoring happens in the student's browser. Nothing is sent to a server, stored, or tracked. The only data that leaves the page is what a student chooses to download or print.

**Customizing.** In the script block near the bottom of `index.html`:

- `CONFIG.course` adds your course name to the header and printouts.
- `NORMS` holds the means and standard deviations used for percentiles. Once you have class data, you can replace the defaults with your own.
- `ITEMS` holds the statements (see above).

---

## Intended use and limitations

This inventory is designed for teaching about personality psychology and for student self-reflection. It is not a clinical, diagnostic, or selection instrument, and scores should not be used for grading, placement, admissions, or hiring decisions.

- Scores are based on self-report and reflect how students see themselves.
- Percentiles compare students with approximate adult norms, not with their classmates.
- Each facet is measured by only two statements, so facet scores are less reliable than trait scores.
- Interpretive text summarizes average patterns from published research. It describes tendencies across many people and does not predict any individual's outcomes.

---

## The 30 statements

Items are presented in this order. "R" marks reverse-scored items.

| # | Statement | Facet | Domain | Scoring |
|---|---|---|---|---|
| 1 | I talk to a lot of different people at parties. | Sociability | Extraversion | |
| 2 | I feel sympathy for people who are worse off than I am. | Compassion | Agreeableness | |
| 3 | I leave my belongings around. | Organization | Conscientiousness | R |
| 4 | I worry about things. | Anxiety | Neuroticism | |
| 5 | I believe in the importance of art. | Aesthetic Sensitivity | Openness | |
| 6 | I wait for others to lead the way. | Assertiveness | Extraversion | R |
| 7 | I insult people. | Respectfulness | Agreeableness | R |
| 8 | I get chores done right away. | Productiveness | Conscientiousness | |
| 9 | I feel comfortable with myself. | Depression | Neuroticism | R |
| 10 | I love to read challenging material. | Intellectual Curiosity | Openness | |
| 11 | I am always on the go. | Energy Level | Extraversion | |
| 12 | I believe that others have good intentions. | Trust | Agreeableness | |
| 13 | I shirk my duties. | Responsibility | Conscientiousness | R |
| 14 | I have frequent mood swings. | Emotional Volatility | Neuroticism | |
| 15 | I do not have a good imagination. | Creative Imagination | Openness | R |
| 16 | I prefer to be alone. | Sociability | Extraversion | R |
| 17 | I am not interested in other people's problems. | Compassion | Agreeableness | R |
| 18 | I like order. | Organization | Conscientiousness | |
| 19 | I am relaxed most of the time. | Anxiety | Neuroticism | R |
| 20 | I do not enjoy going to art museums. | Aesthetic Sensitivity | Openness | R |
| 21 | I take charge. | Assertiveness | Extraversion | |
| 22 | I respect others. | Respectfulness | Agreeableness | |
| 23 | I find it difficult to get down to work. | Productiveness | Conscientiousness | R |
| 24 | I often feel blue. | Depression | Neuroticism | |
| 25 | I avoid philosophical discussions. | Intellectual Curiosity | Openness | R |
| 26 | I like to take it easy. | Energy Level | Extraversion | R |
| 27 | I suspect hidden motives in others. | Trust | Agreeableness | R |
| 28 | I keep my promises. | Responsibility | Conscientiousness | |
| 29 | I rarely get irritated. | Emotional Volatility | Neuroticism | R |
| 30 | I have a vivid imagination. | Creative Imagination | Openness | |

Responses use a five-point scale from *Disagree strongly* (1) to *Agree strongly* (5). Reverse-scored items are recoded as 6 minus the response. Facet scores are the mean of their two items; trait scores are the mean of their three facets.

---

## How to cite this tool

[Your Name]. ([Year]). *Big Five Personality Inventory* [Web application]. [URL]. Facet structure adapted from Soto and John (2017); items from the International Personality Item Pool.

---

## License

- **Code and original interpretive text:** [Choose a license, e.g., MIT for code and CC BY 4.0 for text.]
- **Inventory statements:** International Personality Item Pool, public domain.
- **BFI-2 items:** If you substitute them, they remain copyright 2015 by Oliver P. John and Christopher J. Soto and are not covered by this repository's license.

"FiveThirtyEight" and "538" are trademarks of their respective owners and are mentioned here only to describe this project's history.

---

## References

Asendorpf, J. B., Borkenau, P., Ostendorf, F., & van Aken, M. A. G. (2001). Carving personality description at its joints: Confirmation of three replicable personality prototypes for both children and adults. *European Journal of Personality, 15*, 169–198.

Bogg, T., & Roberts, B. W. (2004). Conscientiousness and health-related behaviors: A meta-analysis of the leading behavioral contributors to mortality. *Psychological Bulletin, 130*, 887–919.

Carney, D. R., Jost, J. T., Gosling, S. D., & Potter, J. (2008). The secret lives of liberals and conservatives: Personality profiles, interaction styles, and the things they leave behind. *Political Psychology, 29*, 807–840.

Chamorro-Premuzic, T., & Furnham, A. (2003). Personality predicts academic performance: Evidence from two longitudinal university samples. *Journal of Research in Personality, 37*, 319–338.

Costa, P. T., Jr., & Piedmont, R. L. (2003). Multivariate assessment: NEO-PI-R profiles of Madeline G. In J. S. Wiggins (Ed.), *Paradigms of personality assessment*. Guilford Press.

DeYoung, C. G. (2006). Higher-order factors of the Big Five in a multi-informant sample. *Journal of Personality and Social Psychology, 91*, 1138–1151.

Digman, J. M. (1997). Higher-order factors of the Big Five. *Journal of Personality and Social Psychology, 73*, 1246–1256.

Feist, G. J. (1998). A meta-analysis of personality in scientific and artistic creativity. *Personality and Social Psychology Review, 2*, 290–309.

Goldberg, L. R., Johnson, J. A., Eber, H. W., Hogan, R., Ashton, M. C., Cloninger, C. R., & Gough, H. G. (2006). The International Personality Item Pool and the future of public-domain personality measures. *Journal of Research in Personality, 40*, 84–96.

Hudson, N. W., & Fraley, R. C. (2015). Volitional personality trait change: Can people choose to change their personality traits? *Journal of Personality and Social Psychology, 109*, 490–507.

Jones, S. E., Miller, J. D., & Lynam, D. R. (2011). Personality, antisocial behavior, and aggression: A meta-analytic review. *Journal of Criminal Justice, 39*, 329–337.

Judge, T. A., Bono, J. E., Ilies, R., & Gerhardt, M. W. (2002). Personality and leadership: A qualitative and quantitative review. *Journal of Applied Psychology, 87*, 765–780.

Koerth-Baker, M. (2018). Most personality quizzes are junk science. I found one that isn't. *FiveThirtyEight*. https://fivethirtyeight.com/features/most-personality-quizzes-are-junk-science-i-found-one-that-isnt/ (no longer online)

Koerth-Baker, M., & Wolfe, J. (2019). Most personality quizzes are junk science. Take one that isn't [Interactive quiz]. *FiveThirtyEight*. https://projects.fivethirtyeight.com/personality-quiz/ (no longer online)

Kotov, R., Gamez, W., Schmidt, F., & Watson, D. (2010). Linking "big" personality traits to anxiety, depressive, and substance use disorders: A meta-analysis. *Psychological Bulletin, 136*, 768–821.

Ozer, D. J., & Benet-Martínez, V. (2006). Personality and the prediction of consequential outcomes. *Annual Review of Psychology, 57*, 401–421.

Poropat, A. E. (2009). A meta-analysis of the five-factor model of personality and academic performance. *Psychological Bulletin, 135*, 322–338.

Roberts, B. W., Walton, K. E., & Viechtbauer, W. (2006). Patterns of mean-level change in personality traits across the life course: A meta-analysis of longitudinal studies. *Psychological Bulletin, 132*, 1–25.

Robins, R. W., John, O. P., Caspi, A., Moffitt, T. E., & Stouthamer-Loeber, M. (1996). Resilient, overcontrolled, and undercontrolled boys: Three replicable personality types. *Journal of Personality and Social Psychology, 70*, 157–171.

Soto, C. J., & John, O. P. (2017a). The next Big Five Inventory (BFI-2): Developing and assessing a hierarchical model with 15 facets to enhance bandwidth, fidelity, and predictive power. *Journal of Personality and Social Psychology, 113*, 117–143.

Soto, C. J., & John, O. P. (2017b). Short and extra-short forms of the Big Five Inventory–2: The BFI-2-S and BFI-2-XS. *Journal of Research in Personality, 68*, 69–81.

Steel, P. (2007). The nature of procrastination: A meta-analytic and theoretical review of quintessential self-regulatory failure. *Psychological Bulletin, 133*, 65–94.

Steel, P., Schmidt, J., & Shultz, J. (2008). Refining the relationship between personality and subjective well-being. *Psychological Bulletin, 134*, 138–161.

Stoeber, J., & Otto, K. (2006). Positive conceptions of perfectionism: Approaches, evidence, challenges. *Personality and Social Psychology Review, 10*, 295–319.

Zuckerman, M. (2007). *Sensation seeking and risky behavior*. American Psychological Association.
