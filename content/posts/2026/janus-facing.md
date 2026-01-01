---
title: recapping 2025, planning 2026
date: 2026-01-01T12:30:00.000Z
---
### stuff i learned at work

a non-exhaustive list of tasks that took not a lot of time individually but i learnt something from because it was my first time doing them

- instrumenting API requests with metrics tracking
- timestream / time series DB usage
- contexts in golang
- appropriate usage of AES / DES cryptographic primitives
- making grafana charts and alerts out of collected data
- PowerBI API usage
- templating web pages with [templ](https://templ.guide/)
- server-state-less auth with JWTs in cookies
- consuming OAuth2
- automated unit testing, mocking, and table tests
- making and tracking custom error types in golang, with wrapping and reflection for effective stack traces
- effective structured logging with loki + grafana integration for dashboard level visibility / aggregation / throttling of relevant data points
- running unit tests and linters in CI jobs
- JSONSchema
- customising linting with GolangCILint. tuning sophisticated linters for validating cognitive complexity, dead code, variable naming conventions, etc.
- documenting APIs with auto-generated OAS docs.
- tuning Dockerfiles for performance and running them locally for testing environment / deployment bugs.
- various HTTP and REST semantics - including:
	- usage of RESTful paths / headers / variables for communication of information
	- effective naming conventions for RESTful APIs
	- correct usage conventions for different HTTP methods, and appropriate status codes
- cleaning other people's dirty API request collections with paramterisation and generalisation
- using [earthboundkid/requests](https://github.com/earthboundkid/requests) for a cleaner request client. usage of custom transports for mocking HTTP requests without mocking the HTTP layer. logging of HTTP requests
- modular mutli-service applications with minimum effort plug and play
- integrating and inspecting redis cache (distributed caches in general really)
- XML basics, calling SOAP APIs
- OAuth1 (lowest point of the year)
- automating OAuth1 signing inside Bruno through a python script (i gave up on crypto in JS)
- automated PDF rendering with [chrome-headless-shell](https://developer.chrome.com/blog/chrome-headless-shell)
- managing and loading AWS secrets
- lambda functions, log monitoring over Cloudwatch, exposing them over API gateway, and interpreting pricing for all of those things
- usage of DynamoDB
- designing and using OAuth2 custom scopes
- Golang HTML string templates for fixed template EMails
- mocking HTTP and SQL requests for testing external services without integration environment setup
- observing DB timeouts in Go applications, monitoring for DB connection leaks, and turning those into actionable observability metrics
- querying AWS Athena DBs and integrating them in Go
- using [go-playground/validator](https://github.com/go-playground/validator) for validating user inputs before processing data
- instrumenting APIs with Prometheus for tracking request latency, volumes, and errors. also includes PromQL and key concepts like histograms vs. summaries
- seamless caching for DB queries to tables that don't change frequently
- heavily involved integration testing for replacing legacy APIs including:
	- full DB schema replication
	- selective data generation / loading for test cases
	- reporting regressions / deviations at a row-level granularity

#### other items in non-chronological order

most of the stuff above went into production code. most of the stuff here involves local scripts.

- Nushell scripting for efficient scrappy data manipulation
- running dotnet projects, and failing miserably to do the same on MacOS
- rudimentary excel scripting for that kind of stuff
- SQL > Pandas > Excel pipeline for internal reports, and the strengths of each of those

#### non-code items

- switched from VSCode to Zed. much better, but still waiting for better low DPI rendering ;-;
- co-ordinating and negotiating project requirements 
- effective limited LLM usage. tried out MCPs but GitHub MCP auth is incorrigible
- giving technical presentations for introducing new technology to teams
- sharing specs with other teams, helping them in implementing their own projects, and an unfortunate amount of debugging on their behalf
- overseeing the work of interns and helping them learn stuff
- giving and receiving code reviews
- taking code interviews
- incremental safe deployment for large replacements to sensitive legacy code
- making flow / sequence diagrams and docs to explain elaborate projects
- added obsidian to my flow for making work documents and syncing them on the team cloud

### stuff i did outside of work

- lua! made a [balatro mod](https://github.com/nyanko-army-knife/nyankatro)
- rust! for this year's [AoC](https://github.com/draconacht/aoc2025)
- some volunteering work, including a static site [Hugo project](https://github.com/draconacht/tgpwu-demo) and some site management with (headless) Sveltia CMS.
- half-baked [LLM API programming](https://github.com/draconacht/secret-llm-project) in Rust
	- muh [htmx](https://htmx.org/) (just a bit)
	- learnt templating with [handlebars](https://handlebarsjs.com/) 
- resuscitated a [battle cats discord bot](https://github.com/nyanko-army-knife/catbot) in [discord.py](https://discordpy.readthedocs.io/en/stable/)
	- experimented with [msgspec](https://github.com/jcrist/msgspec) for explicit schemas
	- learnt and tuned some [fuzzy searching](https://pypi.org/project/RapidFuzz/)
- half-baked gamedev in Godot
	- [cool game with bullet patterns](https://github.com/draconacht/danmakuul)
	- [a finite-state-machine based platformer demo](https://github.com/draconacht/fsm_demo)
- tried to make an API in [fuego](https://go-fuego.dev/), but it isn't for me, i think
- tried to learn Svelte, but it [didn't get far](https://github.com/nyanko-army-knife/nyankopedia)
- moved my domain registrar from name.com to cloudflare
- learnt to profile programs and read traces to measure performance and correct perf bugs
- automated tracking my investments and card spends
- wrote a few blog posts that kinda slap i think

### things i want to do in 2026

- a custom ETL engine in Go, Rust, or both
- more json-schema, OAS, SQL->schema codegen
- a batteries included router in Go, with fiber or net/http
- make an actual factual game
- finish or develop upon at least some of my personal projects
- do any frontend development whatsoever using TS / JS, even if i hate it
- something involving graphics, because those are cool
- RiiR
- figure out something new to do AoC in 
- overthink customising vim keybinds

### non-code plan things

- played a lot of games last year (sts, silksong, yakuza0, ror2, cuphead, a few indie roguelikes, signalis, va11ha11a, halo2, oneshot, elden ring, etc.) sure wanna play more this year (looking at you, bg3). looking forward to sts2 and mewgenics coming out soon.
- use discord / twitter less. go outside more (when it's not trying to kill you (very rare))
- talk to more people in person and go to conferences
- figure out my exit strategy from this job and how to not lose knowledge / talent in the process
- do good things, probably actually volunteer somewhere
- last year was stable for exercise stuff, want to reach new heights in '26
- finances were balanced in 2025 and should be balanced in 2026 as well all things considered
- find cuntier things to wear and wear them
- try to get into fencing, even if it's impossible
- write more blog posts that suck less and get actual readers