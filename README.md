AI Prompt Library
A collection of case studies documenting the architecture, design decisions, and prompt
engineering patterns behind custom GPT deployments built for real clients across
different industries.
What's here:
Each entry documents a production or demo GPT — not the raw prompts, but the thinking
behind them: how they're structured, why certain decisions were made, and what patterns
proved effective in real-world use.
Who this is for:
Teams evaluating my work, collaborators exploring GPT architecture patterns, or
practitioners looking for real-world implementation references.

Cases
GPTDomainModulesKey PatternsHR AI AssistantHuman ResourcesRecruitment, Onboarding, 360 Evaluation, Labor LawKeyword routing, step-locking, two-layer architecture
Neuromarketing ConsultantBehavioral Design & CoachingBrand positioning, Biometric consulting, Wellness coachingLiteral text enforcement, re-engagement loops, lead gen hooksDigital 
Marketing AgencyBrand & Content StrategyIdeal customer profile, Digital audit, Profile optimization, Content planningJSON-structured instructions, internal state tracking, cross-module state inheritance
VEO 3 Prompt GeneratorAI Video ProductionSingle-module brief-to-JSON transformer Bilingual field-level control, no-empty-fields rule, output-only designSustainable 
E-CommerceRetail & LATAM CommerceBrand positioning, Personal care, Pet productsDual-persona design, JSON catalog as source of truth, WhatsApp hand-off
Nonprofit Volunteer OnboardingSocial Impact & EducationTimeline-based preparation guideEthical design layer, anti-persona definition, emotional intelligence module

Recurring Patterns
Across these deployments, a few architectural patterns appear repeatedly:
Keyword-based routing — conversation starters that activate specific modules,
keeping the system prompt clean and each module independently maintainable.
Step-locking with confirmation gates — the GPT cannot advance until the user
explicitly confirms completion of the current step. Critical for process-integrity
workflows where partial inputs produce bad outputs.
Two-layer architecture — system prompt handles routing and persona; knowledge
documents handle process logic. Separating these layers makes systems easier to
update and debug.
JSON as single source of truth — product catalogs, pricing, and structured data
live in a JSON knowledge document. The GPT is prohibited from improvising values
not found there. Eliminates hallucination risk in commercial contexts.
Ethical and scope governance — explicit constraints on what the GPT can say,
what persona it adopts, and what topics it refuses to engage with. Not an afterthought
— a core architectural component, especially in nonprofit, healthcare, and
values-driven brand contexts.

Built by Rodrigo Espinosa Quinteros
Guatemala 🇬🇹 | AI Automation Architect | Bilingual EN/ES
