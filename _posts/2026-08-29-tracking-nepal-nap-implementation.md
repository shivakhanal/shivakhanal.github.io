---
layout: post
title: "Can We Quantify NAP Implementation? An Initial Idea on a Shiny-Based Reporting System for Nepal's Climate Adaptation Progress"
date: 2026-08-29
tags: [climate-adaptation, NAP, Nepal, forest-fire, transparency, R, Shiny]
---

Last week I was invited as a Mentor at the [2026 UNFCCC-CASTT Adaptation Academy](https://unfccc.int/castt-adaptation-academy) for Asia and the Pacific, hosted at the UNITAR Jeju International Training Center in Jeju, Republic of Korea. Over four days, climate policy officials from across the region worked through the practicalities of drafting BTR2, reporting adaptation results, and, the theme I care most about figuring out how to actually *measure* whether adaptation plans are being implemented.

I presented a small tool I've been building: a tracking system for Nepal's National Adaptation Plan (NAP, 2021–2050). The session was well received by participants from a wide range of countries, several of whom are wrestling with the same underlying question in their own contexts. So it seemed worth writing up here.

## The problem with a 300-page plan

Nepal's NAP lays out 64 priority programmes across 10 sectors, with targets specified as narrative text and five-year milestones running out to 2050. That's a serious planning document  but it isn't a monitoring system. There's no structured way to ask, "are we on track for 2025? For 2030?" Progress reporting, where it exists at all, is scattered across agency websites, portals, and one-off reports.

This is a familiar gap in adaptation policy generally: plans are comprehensive, but progress is not centrally quantified, so implementation review tends to default to anecdote.

## The approach

The system pulls the NAP apart into something a computer  and a policymaker  can actually query:

1. A Python-based extraction step structures the targets buried in the NAP PDF into an **indicators master table** (195 indicators across the 10 sectors).
2. Public-source research populates a **progress dataset**, sourcing actual values against each indicator wherever official data exists.
3. An R/Shiny dashboard and an auto-generated PDF report surface the results, filterable by sector, indicator, and status (on track, off track, overdue).

The three outputs: The Shiny app, the PDF report, and a slide deck like the one I presented in Jeju, all run off the same two CSVs, so nothing has to be manually re-typed as new data comes in. Re-knit the report, and every chart updates.

![The Shiny app](/images/napshiny_preview.jpg){: width="600"}
*The Shiny dashboard — filterable by sector, indicator, and status.*

Right now, 29 of the 195 indicators have a sourced progress value, a rough start, not a finish line. Sourcing the rest, sector by sector, is the immediate next phase.

## Why I keep coming back to forest fires

My own path into this work started in fire ecology, so the wildfire indicator is where I look first, and it's a useful illustration of what the system is for.

The NAP targets a **50% reduction** in forest fire incidence by its target year. The observed trend so far is an **increase of roughly 15%**. That's not a subtle miss, it's a target moving in the opposite direction from where it's supposed to be going. A system like this doesn't fix that on its own, but it makes the gap visible and specific, rather than something that stays buried in a narrative progress report until someone asks the right question at the right meeting.

Other indicators tell more encouraging stories. The BIPAD disaster early-warning portal, for instance, is operational *ahead* of its NAP target date, a reminder that the system should flag positive deviations too, not just shortfalls. Local Adaptation Plans of Action are at 270 of 753 local governments completed. New EV sales share is well ahead of pace, even though the total EV fleet share still lags behind the 2030 target. Different indicators, moving at different speeds, all sitting in the same structured table.

## Where this goes next

The near-term priorities are straightforward: keep sourcing progress values across the remaining sectors, backfill time series where possible so single-point comparisons (like the forest-fire chart above) become real trend lines, and keep the reporting outputs re-knitting automatically as the underlying data grows.

The broader question, one that came up repeatedly in conversations with fellow Mentors and participants in Jeju, working on their own countries' BTR2 and NAP tracking, is whether a lightweight version of this approach could be adapted elsewhere. The indicator-extraction and progress-tracking structure isn't Nepal-specific; the sectors and targets change, but the need to turn a planning document into a queryable dataset does not.

If you're working on adaptation tracking in your own country and want to compare notes, I'd be glad to talk, reach me through the contact details on this site.

*Slides from the Jeju presentation and further technical notes on the extraction pipeline are available on request.*
