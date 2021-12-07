# Perfectionists Need To Learn 'sed'

## Table of Contents

1. [Overview](#overview)
2. [Examples](#examples)
3. [Resoureces](#resoureces)

---

## Overview

The sed command, or Stream EDitor, can be a scary command for terminal beginners, and often an underutilized command for intermediate users. The documentation is quite long, cumbersome, and composed largely of error-related comments.

---

## Examples

Sed most recently surfaced for me when working with <code>kubectl</code>, the command utility for managing kubernetes clusters. I did not like how the output was being formatted, so I wanted to columnize it. Sed was the first method that came to mind since I knew I could use regex to find where I wanted insert newlines. [In hindsight, the output was actually formatted correctly - my terminal window was just not wide enough.]

This is what I came up with:

<code>kubectl config get-contexts | tr -s " " | sed -e "s/ /\n/g"</code>

Let's break this command down before moving on to more general examples.

Markdown can only do so much, so here is an image I generated using LaTeX:

---

## Resources