# Data Ethics and AB Testing

## Introduction

When using A/B testing as a method to optimize websites, ad campaigns and more, we may tread potentially dangerous waters when it comes to ethics. Often the purpose for A/B testing is to maximize revenue or optimize some other metric, but it's also important to consider user impact when building A/B tests.

## Objectives

You will be able to:

* Describe the ethical considerations of low-stakes and high-stakes A/B testing
* List the three ethical areas of application in the Belmont Report

![graphic of phones showing A and B](https://www.ama.org/wp-content/uploads/2018/12/a-b-test-ethics.gif?resize=735%2C330)
<p><small>Image credit&nbsp;<a href="https://www.ama.org/marketing-news/are-a-b-tests-ethical/">American Marketing Association</a></small></p>

## Ethical Concerns with a Classic Example

Some A/B tests are low-stakes, like the classic example of *the color of a button*. One might wonder how there could possibly be ethical concerns about this kind of test! However there are two relevant ethical considerations: usability and consent.

### Usability

Often in the tech world, user interface design choices are determined by aesthetic preferences or trends, and these choices may or may not result in the most usable products. Companies with more resources might have in-house or contracted [usability testing](https://www.usability.gov/how-to-and-tools/methods/usability-testing.html) teams, but this will always be limited in the number of participants they are able to recruit prior to launching the product.

A/B testing can be ethically beneficial because it might flag usability issues that were not apparent during the initial testing phase. And concepts like statistical power can help teams to determine how many users should be in each test group.

### Informed Consent

#### Human Subjects Research

Traditionally when you experimentally manipulate conditions in order to understand their impacts on people, that is considered to be [human subjects research](https://www.hhs.gov/ohrp/education-and-outreach/online-education/human-research-protection-training/lesson-2-what-is-human-subjects-research/index.html). Many research institutions have [institutional review boards (IRBs)](https://www.fda.gov/about-fda/center-drug-evaluation-and-research-cder/institutional-review-boards-irbs-and-protection-human-subjects-clinical-trials) specifically dedicated to ensuring that ethical practices are followed when performing human subjects research, particularly medical research.

#### The Belmont Report

The ethical standards applied by IRBs to human subjects research are rooted in the [Belmont Report](https://www.hhs.gov/ohrp/regulations-and-policy/belmont-report/read-the-belmont-report/index.html) of 1976. This report was produced by the Belmont Commission in the wake of the [Tuskegee Syphilis Study](https://www.cdc.gov/tuskegee/timeline.htm), a notoriously unethical study that recruited African-American men with syphilis and withheld modern treatment in order to study the effects of the untreated disease.

The Belmont Report lists three practices that are necessary for ethical human subjects research, the first of which is ***informed consent***. Informed consent means that three elements must be present:

1. Research subjects (now more commonly referred to as _participants_) must be given **information** about the research procedure
2. They must **comprehend** the information that they are given
3. Their participation in the study must be **voluntary**

Because these standards were developed for medical research, they may seem excessive for an A/B testing context. In general following the recommendations in the Belmont Report is only mandatory for researchers working in academic or government institutions, not for data professionals working in industry.

But even in a low-stakes A/B test like changing the color of a button, consider how you might be able to get informed consent, and what negative consequences might arise from not doing so. You may be legally covered by mentioning A/B testing in a "Terms and Conditions" page, but newer [European regulations](https://www.convert.com/blog/privacy/analytics-and-a-b-testing-cookies-only-after-consent-in-europe/) are requiring explicit consent, and this is increasingly seen as an ethical norm.

## Higher-Stakes Ethical Concerns

Perhaps the most high-profile A/B test of the 21st Century so far is the Facebook "emotional contagion" study published in 2014, formally titled [*Experimental evidence of massive-scale emotional contagion through social networks*](https://www.pnas.org/doi/10.1073/pnas.1320040111). This study used Facebook's A/B testing tools as well as natural language processing (NLP) techniques to manipulate the news feeds of over 600,000 Facebook users. Some users had posts with "negative emotional content filtered out, while others had posts with "positive emotional content" filtered out, and then researchers measured the impact of these changes on the "emotional content" of those users' future Facebook posts.

There was broad backlash to this study, in part because there had been no informed consent process ([not even in the ToS](https://www.forbes.com/sites/kashmirhill/2014/06/30/facebook-only-got-permission-to-do-research-on-users-after-emotion-manipulation-study/)). But possibly what angered the public the most was Facebook not following the two other ethical areas of application from the Belmont Report: assessment of risks and benefits, and ethical selection of subjects.

### Assessment of Risks and Benefits

While the Belmont Report does not state that human subjects research must be risk-free, it does say that there should be a "systematic assessment of risks and benefits". Those benefits include "anticipated benefit to society in the form of knowledge to be gained from the research" while risks include "risks of psychological harm, physical harm, legal harm, social harm and economic harm".

The stated benefit of the "emotional contagion" study was to learn whether the emotional contagion observed in in-person studies also occurred in large online social networks. The main risk pointed out by critics was that Facebook was [potentially causing depression](https://www.dailymail.co.uk/news/article-2674469/Facebook-users-depressed-secret-research-Site-deleted-positive-comments-friends.html) in its users. Activists and politicians argued in response that this risk was not worth the stated benefit.

An alternative to A/B testing in a sensitive context like this could be a data mining approach, as in [this paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8700837/), which collected and analyzed already-existing data from an online depression community rather than performing an experiment that manipulated people's online experiences. This may not meet the "gold standard" of a randomized controlled trial in terms of statistical strength but may provide comparable insights with much lower risk to users.

### Ethical Selection of Subjects

The final application area listed in the Belmont Report is the ***ethical selection of subjects***. Subjects must be ethically selected on a social and individual level, and researchers should consider distributive justice in choosing subjects due to "social, racial, sexual and cultural biases institutionalized in society". It also emphasizes that vulnerable subjects should receive additional protections "because they are easy to manipulate as a result of their illness or socioeconomic condition".

The "emotional contagion" study concerned activists because participants appeared to have been chosen randomly, and potentially-vulnerable people experiencing depression or [under the age of 18](https://www.forbes.com/sites/kashmirhill/2014/06/30/facebook-only-got-permission-to-do-research-on-users-after-emotion-manipulation-study/) were apparently not excluded from the study.

In response to concerns about the study, Facebook CTO Mike Schroepfer posted [this update](https://about.fb.com/news/2014/10/research-at-facebook/) to Facebook's research practices. It acknowledged that this particular study could have been done non-experimentally, and also established a new framework for research ethics:

> **Guidelines**: we’ve given researchers clearer guidelines. If proposed work is focused on studying particular groups or populations (such as people of a certain age) or if it relates to content that may be considered deeply personal (such as emotions) it will go through an enhanced review process before research can begin. The guidelines also require further review if the work involves a collaboration with someone in the academic community.

Note how the examples of "particular groups or populations" corresponds to the ethical selection of subjects application area, and "content that may be considered deeply personal" corresponds to the assessment of risks and benefits application area. Facebook also established "a panel including our most senior subject-area researchers, along with people from our engineering, research, legal, privacy and policy teams, that will review projects falling within these guidelines" that resembles an IRB.

Even though following the Belmont Report is not mandatory for a company like Facebook, its basic principles have proven relevant in the 21st Century.

## Additional Resources

* [YouTube video about the Belmont Commission](https://youtu.be/M6AKIIhoFn4)

## Summary

Ethical concerns can arise from performing A/B tests as well as from failing to perform them. A/B tests can help to reveal usability issues that otherwise might have gone unnoticed. However they also can have negative ethical consequences if the Belmont Report application areas of informed consent, assessment of risks and benefits, and ethical selection of subjects are not applied. These negative consequences can be more severe for high-stakes A/B tests but also apply to low-stakes tests like changing the color of a button.
