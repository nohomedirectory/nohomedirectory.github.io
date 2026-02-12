---
layout: post
title: "Day 1: The Plan"
date: 2026-02-11
categories: [journey, planning]
---

Last night I slept in the woods. It was 30 degrees. Today I'm at the library with a laptop, some donated Claude Code passes, and 12 hours to start building.

## The Project

I'm building a clean-room, memory-safe PDF renderer and generator in Rust. Every major PDF library in the world today is either written in C/C++ with decades of security vulnerabilities, or it's painfully slow. There's no fast, safe, modern alternative.

I've never written a line of Rust.

## Why That Doesn't Matter

I don't write code line by line anymore. I direct AI coding agents — primarily Claude Code — using detailed architectural specifications. My job is to be the architect: understand the problem space, design the system, write the spec, and steer the agents.

## What I Did Today

I arrived at the library around 9am and dove into research on the problem space, using Claude and GPT 5.2 Pro to start mapping the landscape — what exists, what's broken, and where the opportunity is.

The core insight: PDF is the de facto document interchange format, and every existing implementation (Poppler, MuPDF, the various Java/Python libraries) is either C/C++ with decades of CVEs or painfully slow. A correct, memory-safe, fast PDF engine would be used everywhere — browsers, enterprise document pipelines, you name it.

I got some solid advice from Jeffrey (@doodlestein): show Claude my spec and have it produce one like his FrankenTUI spec but for PDF. Get a complete open-source PDF renderer/generator in TypeScript as reference, then build it in Rust.

From there, I started shaping the spec (still currently incomplete, but the skeleton is forming):

- **Core deliverable**: A library — a Rust crate that other projects depend on.
- **Demo/showcase**: Compile to WASM for a browser-based demo hosted on GitHub Pages right from the repo — drop a PDF in, watch it render, generate a new one. That's powerful for the blog.
- **CLI tools**: `pdfrender input.pdf output.png`, `pdfgen template.json output.pdf`. These aren't mutually exclusive — they're just different frontend binaries consuming the same core library crate.

The goal crystallized: create the world's best and most performant, memory-safe Rust PDF renderer/generator. The blog post I want to write at the end: *"How I took a bunch of donated Claude passes and turned it into the world's best and most performant, memory-safe Rust PDF renderer and generator."*

The AI agent workflow is central to all of this. I act as a thought partner during ideation, an orchestrator during planning, and a very distant manager during implementation and testing. The coding system will be designed as a closed loop — the human (me) should never be the bottleneck on AI agent productivity. That will come later, after the ideation and planning phase.

It's important to consider the new agent capabilities that are at our disposal. This project is indeed very ambitious, but the goal here is to show just what is possible with the new AI coding agents, and astonishingly, at such a fast rate, by a literal homeless man in a public library, taking only days to produce. Yes, this is ENTIRELY realistic.

### The Failure

I said I'd chart my failures alongside my successes, so here's the first one.

I couldn't focus. Too much in my head at once. Around 4:30pm — having arrived at 9am — I left. I went on a walk to a rather secluded spot to collect myself.

That's a failure. I had 12 hours of library time and used roughly 7, with much of it scattered. When you're dealing with homelessness and trying to build ambitious software simultaneously, the mental load is brutal. Walking away was the right call for my head, but I need strategies to not need to walk away in the first place.

### That Night

That night it was 30 degrees and I slept out in the woods. I stuffed my pants with some of my clothes for extra insulation.

![Pants stuffed with clothes for warmth in 30-degree weather](/assets/images/day1-sleeping-in-the-cold.jpg)

## What I Learned

- Mapping the problem space is real work, even when it doesn't feel like "building." Understanding what exists and what's broken is the foundation everything else sits on.
- I need to be more deliberate about managing the noise in my head. The mental overhead of homelessness doesn't pause while you're trying to architect software.
- The spec is taking shape. A Rust crate as the core, WASM for the demo, CLI tools as frontends. The vision is clear.

---

*This is post #1 of an ongoing series. I'll be writing daily about what I build, what works, what doesn't, and what it's like to do this from a library with nothing.*
