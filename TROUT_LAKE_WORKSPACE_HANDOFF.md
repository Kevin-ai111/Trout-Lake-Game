# TROUT LAKE — WORKSPACE HANDOFF
Version: 2026-10-14
Status: ACTIVE DEVELOPMENT
Project Owner / Authenticity + Fun Gate: Kevin

---

# 1. PURPOSE OF THIS DOCUMENT

This document is the canonical workspace handoff for TROUT LAKE.

Every AI agent/chat working on this project must read this document before
making design, code, art, QA, or roadmap decisions.

This project previously used several separate AI chats and tools.
The project is now continuing inside the Mr.Maks Workspace with multiple
specialized chats.

Do not assume conversation memory is complete.

SOURCE-OF-TRUTH PRIORITY:

1. Current Git repository / exact HEAD
2. This handoff document
3. Repository documentation
4. Explicit current Game Director decisions
5. Chat history / model memory

If chat memory conflicts with Git or this document:
Git / current documentation wins.

---

# 2. PROJECT

Working title:

TROUT LAKE

Repository:

https://github.com/Kevin-ai111/TROUT-LAKE

Current Pull Request:

PR #1 — Fishing Feel Prototype v0.1

https://github.com/Kevin-ai111/TROUT-LAKE/pull/1

Current branch:

codex/fishing-feel-prototype-v0.1

Base:

main

Current known Base SHA:

5d2a2fa90a00b51549c0ecfd772a704b6696935a

Current known HEAD:

d62aa549497f2ef025fef7d864183439eb04078f

IMPORTANT:

PR #1 is currently OPEN and MUST NOT be merged until the current
Fishing Feel validation pipeline is complete.

Before doing any implementation work:

VERIFY THE ACTUAL CURRENT HEAD IN GIT.

Do not blindly trust the SHA in this document if newer commits exist.

---

# 3. ENGINE / TECH STACK

Engine:

Godot 4.7.2 Stable

Language:

GDScript

Renderer:

Forward+

Target:

PC / Steam

Primary target resolution:

1920 × 1080

Secondary validation:

1280 × 720

960 × 540 may be used for UI sanity checks.

Current prototype:

Keyboard + Mouse

Controller support is NOT currently required.

No third-party addons unless specifically approved.

---

# 4. CORE GAME VISION

TROUT LAKE is:

A cozy fishing-life game with incremental progression.

Core fantasy:

"Ein Leben als Angler."

The player should:

- learn through actual fishing experience
- improve personal knowledge
- acquire better and more specialized equipment
- unlock new techniques
- visit increasingly interesting trout lakes
- observe conditions and other anglers
- change tactics when fishing slows down
- feel satisfaction from becoming a more capable angler

This is NOT:

- an idle game
- an automation game
- a clicker with a fishing skin
- a hardcore fishing simulator
- an arcade fishing game
- an RPG stat-buff simulator

The player should improve partly because THEY learn.

Gear should primarily unlock options and techniques.

Avoid generic systems such as:

+15% catch chance
+20% fish strength
+10% luck

Fishing knowledge should matter.

---

# 5. CORE PLAYER MOTIVATION

The player should repeatedly think:

"What should I try next?"

Examples:

- continue the current retrieve?
- change retrieve speed?
- let the lure sink deeper?
- twitch?
- change lure?
- switch technique?
- move fishing spot?
- observe other anglers?
- take a short pause?
- change tackle?

The fishing itself must remain interesting enough before progression
systems are added.

---

# 6. PRIMARY PRODUCT TEST

The current project is NOT testing progression.

It is testing:

FISHING FEEL.

The primary acceptance question is:

"After landing one trout, does Kevin voluntarily want to cast again?"

If the answer is NO:

Do not solve that problem with XP, money, shops, missions, unlocks,
collectibles, or more content.

Fix the fishing.

---

# 7. FIRST LAKE — TANNENWEIHER

The first lake is:

TANNENWEIHER

It is loosely inspired by small managed South German trout lakes.

It must NOT be a direct 1:1 copy of a real commercial fishery.

Target feeling:

- compact
- maintained
- plausible
- German / South German
- forest-edge setting
- walkable banks
- small service hut
- parking nearby
- several possible fishing spots
- cozy rather than spectacular wilderness

Approximate logical lake size:

55 × 30 m

Shape:

elongated irregular oval / light kidney / teardrop form

Approximate depth concept:

Bank:
0.5–0.8 m

Inlet:
0.8–1.2 m

Main body:
1.3–1.8 m

Deep corner:
2.0–2.5 m

Potential future conceptual spots:

P1 — Hauptufer
neutral beginner / all-round

P2 — Zulauf
shallower / oxygen rich / morning activity

P3 — Schilfkante
precision / observation

P4 — open long side
good for active Spoon fishing

P5 — deep corner
useful during warmth / sun

P6 — transition / route area
variable fish traffic

DO NOT expose hidden bonuses like:

"P2 +15% catch rate"

Fish should move and behave according to conditions.

---

# 8. CURRENT PROTOTYPE LOCATION

Fishing Feel Prototype v0.1 currently uses:

ONE fishing position only.

The full lake is NOT required yet.

Camera is a controlled gameplay composition rather than a free-roaming
third-person world.

---

# 9. ART DIRECTION — APPROVED

Approved direction:

STYLIZED REALISTIC 3D
presented as a controlled 2.5D PLAYABLE DIORAMA.

Interpretation:

- actual 3D environment
- actual 3D angler
- actual 3D trout
- stylized materials
- controlled composition
- grounded natural atmosphere
- painterly / game-ready appearance
- not photoreal
- not pixel art
- not exaggerated cartoon

General mood:

- German trout lake
- forest greens
- blue-green water
- earthy bank materials
- warm natural sunlight
- restrained UI
- cozy but believable

Camera:

third-person,
slightly behind and to one side of angler.

Initial art-direction starting values:

camera approximately:
2.3–2.7 m behind
1.2–1.5 m lateral
1.55–1.70 m high
slight downward angle

These are NOT hard technical locks.

Composition matters more than exact values.

Target visual hierarchy:

1. rod + line
2. active water / fish
3. angler
4. opposite bank
5. vegetation
6. HUD

Water should occupy a large part of the playable view.

---

# 10. HERO VISUAL

Primary screenshot / visual fantasy:

ACTIVE FIGHT.

Show:

- strongly bent UL rod
- visible line tension
- fish pulling away
- surface disturbance / splash
- player visibly engaged
- recognizable trout-lake setting

Avoid cinematic camera takeover.

The game should still look playable.

---

# 11. FISH VISIBILITY

Fish are NOT permanently highlighted.

No:

- fish outlines
- fish icons
- floating markers
- permanent x-ray visibility

Depth presentation:

DEEP:
mostly invisible

MID:
shadow / silhouette possible

SHALLOW:
more clearly visible through water

FOLLOW RANGE:
player can clearly recognize a fish following the Spoon

Important emotional beat:

"Da kommt einer hinterher."

Typical visual follow distance:

approximately 0.4–1.0 m behind lure.

---

# 12. FIRST SPECIES

Fishing Feel Prototype:

RAINBOW TROUT ONLY.

German:

Regenbogenforelle.

No other species are required yet.

---

# 13. TANNENWEIHER FISH SIZE PROFILE

Canonical early-game size range:

~200 g minimum

200–300 g:
very common

300–450 g:
common

450–600 g:
occasional

600–800 g:
rare

800–1000 g:
very rare

Fish may slightly exceed 1 kg occasionally in the future.

A roughly 1 kg trout should feel special at the first lake.

IMPORTANT:

This early size profile intentionally leaves progression room for later
lakes with significantly larger trout.

---

# 14. FISH INDIVIDUALITY

Fish difficulty is NOT determined by weight alone.

Current conceptual hidden attributes include:

- weight
- temperament
- stamina
- caution

Core rule:

WEIGHT DETERMINES TENDENCY, NOT EXACT FIGHT DIFFICULTY.

Example:

270 g
aggressive
high stamina

may fight harder than:

620 g
calm
low stamina

But statistically larger fish should still trend stronger.

Avoid RPG stat bloat.

---

# 15. CURRENT FISHING METHOD

Prototype v0.1:

ACTIVE UL SPOON FISHING ONLY.

No:

- float fishing
- dough
- bee maggot
- Sbirolino
- rubber bait
- jigging
- passive rod

Those come later only if Spoon Fishing Feel succeeds.

---

# 16. CURRENT STARTING TACKLE

Concept:

UL rod:
approximately 1.8–2.0 m

Target:
~1.9 m

Casting weight:
approximately 0.5–5 g

Small spinning reel.

Fine trout-suitable main line.

---

# 17. CURRENT SPOONS

Three prototype Spoon profiles only.

SPOON A

~2.0 g
bright / noticeable
slower / shallower tendency

SPOON B

~2.5 g
dark / natural
all-round

SPOON C

~3.0 g
contrasting
slightly faster / deeper

The purpose is to prove meaningful presentation differences.

Do not create a huge lure catalog yet.

---

# 18. CURRENT CORE LOOP

The prototype must support:

prepare cast
→ cast
→ Spoon splashdown
→ sink
→ retrieve
→ vary retrieve speed
→ twitch
→ pause
→ fish notices lure
→ interest
→ follow
→ nibble / strike / abort
→ possible hook-up
→ fight
→ drag management
→ line tension management
→ fish close to bank
→ manual netting
→ catch result
→ cast again

---

# 19. CURRENT CONTROLS

Current intended controls:

1 / 2 / 3
select Spoon

C
simple cast

Hold / release RMB
charged active cast

Hold LMB
retrieve / reel

Mouse wheel during lure fishing
retrieve speed

Mouse wheel during fight
drag

Space
twitch / rod pressure

E
landing net attempt

F1–F10
developer fixtures only

These must NOT be available to normal players unless explicitly enabled
in a debug build.

---

# 20. FISH REACTION STATES

Current architecture includes concepts such as:

CRUISE
NOTICE
INTERESTED
FOLLOW
NIBBLE
STRIKE
ABORT
HOOKED
FIGHT
EXHAUSTED
LANDED
ESCAPED

Do not build a giant generic AI framework.

This is intentionally a purpose-built fishing interaction state machine.

---

# 21. BITE TYPES

Required behaviors include:

HARD STRIKE

Fish commits aggressively.
Hook-up can happen naturally.

CAUTIOUS NIBBLE

Short contact.
Player may benefit from continuing retrieve rather than reacting too hard.

FOLLOW WITHOUT BITE

Fish follows but does not commit.

ABORT

Fish loses interest and turns away.

No giant:

"STRIKE NOW!"

QTE.

Feedback should come through:

- fish
- rod
- line
- water
- later audio

---

# 22. FIGHT DESIGN

Fight is one of the emotional cores of TROUT LAKE.

Player controls:

- reeling
- rod pressure
- drag
- reaction to runs

Possible fish behaviors:

- explosive sprint
- longer horizontal run
- turn toward player
- surface burst
- recovery / lower-force movement

Possible losses:

- slack line
- excessive tension / line break
- failed hook-up

Fight should be approachable but not automatic.

---

# 23. IMPORTANT FIGHT PRINCIPLE

Small fish can fight surprisingly hard.

Large fish are generally harder but not always.

Do not make fight duration deterministic.

Approximate target tendencies only:

200–300 g:
often ~10–20 sec

~500 g:
often ~20–35 sec

800–1000 g:
can reach ~40–60 sec

These are tuning targets, not fixed timers.

---

# 24. MANUAL LANDING

Landing is manual.

Player presses:

E

Fish must be:

- close to shore
- still in water
- sufficiently tired / controlled
- not in a powerful run
- under sensible line tension

Bad net timing should:

NOT automatically lose the fish.

Player can regain control and try again.

No large arcade QTE.

---

# 25. CATCH RESULT

Prototype result should remain simple.

Example:

REGENBOGENFORELLE

347 g

optional:
approximate length

optional:
NEW PERSONAL BEST

Then:

CAST AGAIN

No:

- XP fireworks
- money fireworks
- loot screen

---

# 26. CURRENT GAMEPLAY ARCHITECTURE

Current high-level authority split:

FishingSession
- coordinates overall fishing loop
- cross-system lifecycle ownership

LureController
- authoritative Spoon state / movement
- fish-interactivity state

FishController
- individual trout behavior

FightController
- active fight
- drag
- tension
- line payout
- fish fight movement

LandingController
- landing eligibility
- net action

FishingRodController
- rod presentation / player interaction

PrototypeHUD
- presentation only

PlayableWater
- authoritative prototype playable-water footprint / landing geometry

IMPORTANT:

HUD MUST NEVER OWN GAMEPLAY STATE.

Visual animation MUST NEVER decide whether a fish is caught.

---

# 27. SINGLE-FIGHT OWNERSHIP

One fish only may own an active fight.

Current concept uses:

fight_fish

Once a fight begins:

- that fish remains authoritative
- lure becomes non-interactive for other fish
- other fish abort lure engagement
- unrelated fish cannot steal fight ownership

Do not regress this.

---

# 28. LURE INTERACTIVITY

Fish must only react to an interactive Spoon.

Non-interactive examples:

OUT_OF_WATER
IN_FLIGHT
ATTACHED to hooked fish

A fish must NOT:

- follow lure onto bank
- strike a lure already out of water
- become hooked from stale presentation state
- attack the lure during its cast flight

---

# 29. TEST STATUS — CURRENT HEAD

At current known head:

d62aa549497f2ef025fef7d864183439eb04078f

Reported / independently confirmed test status:

75 passed
0 failed

Godot:

4.7.2 Stable

CI passed on current known head.

However:

THE BUILD IS NOT YET APPROVED FOR HUMAN FISHING-FEEL PLAYTEST.

---

# 30. INDEPENDENT REVIEW WORKFLOW

Current development workflow intentionally uses multiple AI systems.

Recommended roles:

CODE IMPLEMENTATION
Codex / strong coding model

INDEPENDENT CODE REVIEW
Claude Opus

GAME DIRECTION
ChatGPT / Game Director

ART DIRECTION
ChatGPT / visual concept pipeline

QA
independent QA / Work-style agent

FINAL AUTHENTICITY + FUN
Kevin

IMPORTANT:

Do not let Codex and Claude independently edit the same branch in parallel.

Preferred pattern:

Codex implements
→ Claude reviews read-only
→ Game Director decides what matters
→ Codex fixes
→ QA
→ Kevin plays

---

# 31. WHY CLAUDE IS USED

Claude is NOT currently the lead developer.

Claude is used as an adversarial independent reviewer.

This workflow already found important issues that isolated automated tests
did not initially catch.

Use Claude especially for:

- state-machine edge cases
- cross-system lifecycle bugs
- test-quality review
- long simulated sequences
- challenging Codex assumptions

Do not automatically implement every Claude observation.

Severity and milestone relevance matter.

---

# 32. CURRENT OPEN ISSUES

CURRENT HEAD:

d62aa549497f2ef025fef7d864183439eb04078f

The following items are OPEN and should be addressed before the first
human Fishing Feel playtest.

## OPEN P0 / PLAYTEST BLOCKER — Fight Slack Balance

Current independent review found that fights are excessively dominated
by slack losses.

Critical conceptual problem:

Reeling can currently contribute to fish movement toward the player
faster than line can be retrieved.

This means:

the player can perform the correct action
and still CREATE additional slack.

That is unacceptable for the human Fishing Feel evaluation.

Required principle:

REELING TAKES UP LINE.

Reeling should not artificially make the fish approach faster than the
reel can retrieve available line.

TURN_TOWARD without reeling:
should create slack risk.

TURN_TOWARD with prompt reeling:
should usually be recoverable.

Powerful outward run + excessive drag:
should still risk critical tension / line break.

Do NOT tune to an exact bot win rate.

Human playtesting determines final balance.

---

# 33. OPEN P1 — EDGE ESCAPE / CRUISE STALL

After a fish escapes near a water boundary:

home can be set close to the edge.

A generated cruise target may then be outside reachable water.

Because movement is constrained by PlayableWater, the fish can stall
trying to reach an impossible target.

Required:

- generated cruise targets must be valid reachable water positions
- edge escapes must recover into meaningful swimming behavior
- optional no-progress fallback may choose a new valid target

Do not teleport fish during ordinary movement.

---

# 34. OPEN P1 — ROD RESET AFTER LOSS

Possible current ordering bug:

FightController may end a fight during:

simulate_step()

but the same FishingSession frame can subsequently reapply stale:

rod.set_load(fight.tension)

Result:

rod may remain bent during PREPARE.

Required:

After simulate_step:

only apply fight rod load if:

phase == FIGHT
AND
fight.active

Otherwise rod load remains zero.

---

# 35. OPEN P1 — DEBUG FIXTURES DEFAULT

Current known project setting:

prototype/debug_fixtures_enabled=true

For playtesting this must default to:

false

F1–F10 remain available only when deliberately enabled in a debug build.

---

# 36. NEXT DEVELOPMENT TASK

The next code task is:

PR #1 CORRECTION PASS v3

ONLY address:

1. reeling/slack mechanical sanity
2. edge escape / cruise recovery
3. rod load reset after loss
4. debug fixture default false
5. targeted regression tests for those items

Do not expand scope.

---

# 37. AFTER CORRECTION PASS v3

Required sequence:

Codex completes v3
→ exact new Git HEAD recorded
→ CI green
→ Game Director reviews exact diff
→ Claude receives SHORT DIFF RE-REVIEW only

Claude should answer only approximately:

1. Is fight/slack contradiction fixed?
2. Is edge escape stall fixed?
3. Is rod reset fixed?
4. Did v3 introduce a new blocker?

Do NOT start another huge speculative review cycle unless a real blocker is found.

---

# 38. STOP CONDITION FOR CODE PING-PONG

After v3:

If:

- tests pass
- CI passes
- Director finds no blocker
- Claude finds no blocker

STOP theoretical coding iterations.

Proceed to:

ART REVIEW
→ QA
→ HUMAN PLAYTEST

Do not pursue prototype perfection before Kevin plays it.

---

# 39. HUMAN PLAYTEST GATE

Kevin is the Authenticity + Fun Gate.

The core question:

"Willst du freiwillig noch einen Wurf machen?"

Other playtest questions:

1. Is casting understandable?
2. Is retrieve speed noticeable?
3. Does twitch feel responsive?
4. Does letting the Spoon sink feel meaningful?
5. Is seeing a follower exciting?
6. Do bite types feel different?
7. Does rod bend communicate pressure?
8. Is line tension understandable?
9. Does drag feel useful rather than annoying?
10. Do fish feel individually different?
11. Can a small aggressive trout surprise the player?
12. Does manual netting add tension?
13. Do I want another cast?

Question 13 dominates.

---

# 40. CURRENT STRICT OUT-OF-SCOPE LIST

DO NOT IMPLEMENT YET:

- economy
- XP
- levels
- shop
- ticket system
- missions
- fish-selling system
- full day simulation
- weather
- day/night cycle
- multiple lakes
- full Tannenweiher map
- free-roaming player
- spot selection
- NPC anglers
- passive rods
- dough fishing
- bee maggot
- float fishing
- Sbirolino
- jigging
- rubber bait
- equipment durability
- knots
- hook wear
- line wear
- character customization
- boats
- vehicles
- multiplayer
- achievements
- Steam integration
- full save system
- production audio
- final production art

If a developer believes one of these is required:

STOP.

Explain why before implementing it.

---

# 41. FUTURE PROGRESSION — NOT CURRENT IMPLEMENTATION

Later design direction:

XP primarily represents:

experience / eligibility / access.

XP should NOT become:

hidden catch-rate buffs.

Example future progression:

Level unlocks the ability to buy/use:

- better dough
- UL rods
- Spoons
- Sbirolino
- rubber bait
- better leader material
- premium tackle
- later lakes

Unlock does NOT equal free item.

Money will eventually provide purchasing power.

---

# 42. FUTURE ECONOMY — NOT LOCKED

Later:

Caught fish can generate money at end of day.

Missions/orders may add bonuses.

A bad fishing day does not have to guarantee profit.

Exact ticket prices, fish values and economy numbers are NOT currently
canonical.

Do not build economic systems from old illustrative numbers.

---

# 43. FUTURE DAY STRUCTURE — NOT CURRENT

Potential future day length:

approximately 15–20 real minutes.

Possible activity phases:

morning
midday
afternoon

Fish behavior may later change with:

- temperature
- light
- depth
- oxygen
- fish movement

This is future design, not prototype code.

---

# 44. FUTURE NPC ANGLERS

Potential later feature:

2–4 anglers visible around the lake.

Their catches can provide diegetic information.

Example:

Player sees another angler catching at the opposite side
→ may infer fish activity
→ considers moving / changing method.

This reflects real angling behavior.

NOT part of current v0.1.

---

# 45. ART PRODUCTION POLICY

Do not produce expensive/final assets before Fishing Feel succeeds.

Current greybox / placeholder art is acceptable.

Order:

mechanics work
→ Fishing Feel approved
→ art direction refined
→ production assets

Do not use polished visuals to hide weak gameplay.

---

# 46. WORKSPACE CHAT STRUCTURE

Recommended Mr.Maks Workspace chats:

00 — GAME DIRECTOR

Purpose:
vision
scope
milestones
decision authority
commercial / gameplay judgment

Must prevent feature creep.

---

01 — DEV

Purpose:
Godot
GDScript
implementation
tests
CI

DEV implements approved tasks only.

DEV does NOT decide roadmap.

---

02 — CODE REVIEW

Purpose:
independent adversarial review

Preferred reviewer:
Claude Opus

READ ONLY unless explicitly instructed otherwise.

Do not let reviewer silently edit implementation.

---

03 — ART DIRECTOR

Purpose:

- gameplay camera
- composition
- readability
- visual direction
- Tannenweiher look
- HUD direction
- fish/water readability

Concept and direction first.

---

04 — QA

Purpose:

- regression
- runtime
- state integrity
- UI
- input
- performance
- repeatability

QA does not implement fixes.

QA reports.

---

05 — PLAYTEST / FEEDBACK

Purpose:

Kevin's real gameplay observations.

Record:

- what felt good
- what felt wrong
- what was confusing
- what was boring
- what felt authentic
- what felt artificial
- whether another cast felt desirable

Human feedback overrides theoretical AI preferences when deciding
Fishing Feel.

---

# 47. AGENT AUTHORITY

GAME DIRECTOR:

owns:
WHAT / WHY / WHEN

DEV:

owns:
HOW to implement approved technical work

CODE REVIEW:

owns:
finding technical risk

QA:

owns:
verification / reproduction

ART DIRECTOR:

owns:
visual direction

KEVIN:

owns:
AUTHENTICITY + FUN ACCEPTANCE

No agent may silently expand its authority.

---

# 48. DEVELOPMENT RULES

Every development task should start with:

READ BEFORE WORKING:

1. TROUT_LAKE_WORKSPACE_HANDOFF.md
2. docs/PROJECT_VISION.md if present
3. docs/CURRENT_STATE.md if present
4. docs/ARCHITECTURE.md if present
5. docs/DECISIONS.md if present
6. exact current Git HEAD / PR state

Then:

inspect actual code.

Never implement based solely on prompt assumptions.

---

# 49. GIT RULES

Do not:

- force push
- rewrite history
- squash active work without approval
- silently merge
- create giant cleanup refactors
- change unrelated code during a focused correction

Prefer:

small commits
small PR scope
exact SHA reporting
tests attached to bug fixes
CI evidence

Every agent report should include:

Repository
PR
Branch
Base SHA
Head SHA
Tests
CI
Known limitations
Status

---

# 50. BRANCH / PR POLICY

Current work stays on:

codex/fishing-feel-prototype-v0.1

PR #1 remains the current validation vehicle.

Do NOT create:

PR #2

just to fix PR #1 review findings.

Continue correcting the existing branch until accepted.

---

# 51. TESTING PHILOSOPHY

Tests should validate actual runtime behavior where practical.

Avoid tests that claim:

"normal gameplay can reach X"

while manually assigning:

X = almost reached.

Examples to avoid:

- tension preset near failure threshold as only overload proof
- stamina manually exhausted as only landing proof
- teleport fish to landing zone as only proof a fight is winnable

Direct fixture manipulation remains acceptable when testing isolated
state behavior.

But core Fishing Feel needs integration/simulation tests too.

---

# 52. IMPORTANT LESSON FROM CURRENT REVIEWS

Most serious bugs were NOT inside isolated components.

They were at hand-offs between:

Lure
Fish
Session
Fight
Landing

Therefore reviews should pay special attention to:

- invalid state transitions
- reset paths
- signal ordering
- stale references
- repeated loops
- simultaneous fish interactions
- loss → next cast
- catch → next cast

---

# 53. ARCHIVE ZERO

ARCHIVE ZERO is a previous separate project.

It must NOT contaminate TROUT LAKE development.

Do not import:

- archive gameplay concepts
- machine systems
- production lines
- case processing
- Scanner
- Sorter
- Archive Intake
- old UI conventions
- old save architecture
- old visual style

General engineering lessons may be reused.

TROUT LAKE itself is a fresh project.

---

# 54. COMMERCIAL DESIGN PRINCIPLE

TROUT LAKE should be immediately understandable.

A screenshot should communicate:

"Fishing game."

The fantasy should not require explanation.

The project deliberately moved away from systems that require long
conceptual explanation before they become interesting.

---

# 55. DESIGN ANTI-PATTERNS

Avoid:

FEATURE CREEP

"Maybe add this while we're here."

NO.

---

SYSTEMS BEFORE FEEL

Do not build economy/progression before fishing is fun.

---

HIDDEN STAT SOLUTIONS

Do not solve behavior with unexplained:

+10%
+20%
+luck

---

MENU GAME

Fishing should remain the center.

Do not let equipment/progression UI become the actual game.

---

HARDCORE SIMULATION FOR ITS OWN SAKE

Accuracy is valuable only when it improves:

- decision making
- authenticity
- fun
- readability

---

ARCADE QTE OVERLOAD

The player should read:

fish
rod
line
water

not giant UI instructions.

---

# 56. CURRENT DEFINITION OF DONE — FISHING FEEL v0.1

Fishing Feel v0.1 is DONE only when:

- core loop works repeatedly
- no lifecycle blocker exists
- Spoon control is understandable
- twitch matters
- follow behavior is readable
- bites have meaningful variation
- fight is controllable
- drag matters
- slack makes sense
- tension makes sense
- fish can be lost
- fish can realistically be landed
- netting is manual
- next cast works cleanly

AND:

Kevin plays it.

AND:

Kevin voluntarily wants another cast.

Tests alone are NOT enough.

Art alone is NOT enough.

AI reviews alone are NOT enough.

---

# 57. IMMEDIATE NEXT MILESTONE

CURRENT:

Fishing Feel Prototype v0.1

NEXT:

Correction Pass v3
→ short final code review
→ ART runtime review
→ QA
→ Kevin human playtest

ONLY AFTER SUCCESS:

Phase 2 — Fish Behavior / fishing depth and activity refinement.

Later:

second fishing method.

Later:

complete fishing day.

Later:

progression/economy.

---

# 58. FINAL RULE

When uncertain whether a feature should be added now, ask:

"Does this directly help us determine whether one Spoon cast is fun?"

If NO:

it probably does not belong in the current milestone.

END OF HANDOFF