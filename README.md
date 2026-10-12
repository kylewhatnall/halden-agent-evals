# halden-agent-evals

An eval harness for a Slack request drafting agent, built to find where it fails and prove whether fixes work.

## What's being tested

A drafting agent reads marketing requests the way a team posts them in Slack, writes an on brand draft, and declines requests that need a human. It's modeled on a drafting agent I run in production. All requests and company details belong to Halden, a fictional commercial HVAC field service software company. Every piece of data here is invented.

## Status

Week 1, in progress. This README is the only file so far.

## Plan

- Write 100 varied Halden requests and run the drafter on all of them
- Error analysis: read every output and note each failure
- Failure taxonomy: group the failures into 5 to 8 categories
- Golden set of 30 cases with code checks (banned words, length, correct declines)
- LLM judge for the subjective categories, calibrated against human labels
- Fix the biggest failure mode and report before and after results

## What still fails

Nothing measured yet. This section will list known failures after the first eval run.