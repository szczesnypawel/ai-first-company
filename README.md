# AI-first company: data

The data behind **[ai-first.company](https://www.ai-first.company)**, a guide to what works and what fails in running a business with AI. The guide is organised by company size, and every practice on it is rated by how strong the evidence is.

This repository holds three lists from the site, each as JSON and CSV. They are built from the same files as the pages, so they always match what the site shows. They hold the lists only, not the full text of the pages. Each JSON file gives its number of rows in `count`.

| File | What it holds | On the site |
| --- | --- | --- |
| `data/practices.json`, `data/practices.csv` | Practices for running a business with AI, each rated by strength of evidence: summary, theme, stage, company sizes it fits, priority, effort, evidence level and warnings, studies for and against, linked company cases | [Practices](https://www.ai-first.company/practices/) |
| `data/cases.json`, `data/cases.csv` | Named companies that used AI at work: company, business, country, period, size band, how it turned out, who produced the figures, practices the case bears on, public sources | [Company cases](https://www.ai-first.company/evidence/cases/) |
| `data/assessments.json`, `data/assessments.csv` | Published instruments for assessing where a company stands with AI (questionnaires, tests, task maps, interview guides): the question each one answers, type, how well it has been tested, who answers it, length, licence, cost, languages, provider and source publications | [Assessments](https://www.ai-first.company/assessments/) |

## Format

- **JSON:** each file has a short header (`name`, `description`, `url`, `version`, `licence`, `licenceUrl`, `count`) and the list under `rows`. Fields with more than one value are lists. Linked items are objects with an `id`, a `title` and a `url`.
- **CSV:** one row per item, UTF-8. Fields with more than one value are joined with `; `. Cases split linked practices into `practices_applied`, `practices_missing` and `practices_later`.
- **`id`** is the item's address on the site: practice `x` is at `https://www.ai-first.company/practices/x/`.
- **`reviewed`** is the date the item was last checked against its sources. The file's `version` is the newest of these dates.

## How evidence is rated

Practices and assessments use the same scale: **Strong**, **Moderate**, **Emerging**, **Common practice** (widely done, not yet studied) and **Not yet tested**. Case outcomes are **Measured result**, **Company-reported result**, **Went wrong** and **Partly walked back**. The method is described at [How we rate the evidence](https://www.ai-first.company/evidence/how-we-rate/).

## Licence and credit

The data is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (see `LICENSE`). Credit it as:

> Data: CC BY 4.0, Paweł Szczęsny, ai-first.company

The licence covers these data files only, not the text of the site. The sources the lists link to keep their own terms.

## Updates and corrections

The files are updated automatically whenever the site is published with changed lists. The latest version is always available at [ai-first.company/data](https://www.ai-first.company/data/). If you find an error, please open an issue.

Author: Dr Paweł Szczęsny ([about](https://www.ai-first.company/about/))
