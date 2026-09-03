# AI Strategy One-Pager - Juno Automated Prioritization

## 1. Problem & Workflow

The problem is that the loudest voice in the room or Slack gets to dictate the roadmap without critical customer evidence. Priorities are reversed and stakeholder trust is eroding. 

Prevention: Juno explicitly prevents opinion driver prioritization and focuses on data driven corrections focusing of evidence that cites the correction

## 2. Target Metrics

Cycle time: Reduction of product roadmap discussion from 2 hrs to 30 min (a 75% time reduction). Reduction of de-prioritization by a week.

Leadership confidence, 10% of prioritization reversal and 90% of prioritization with 2 cited goals

## 3. Autonomy Level

Copilot

Explicitly avoid: agent that reprioritizes without human in the loop

## 4. Data & Model Approach

Approach: Grounding (RAG) with inputs from Notion, Jira...
Explicitly Avoid: LLM (buy) to avoid hallucinations

## 5. Risks & Mitigations

Risk: training data lag. Juno could over-weight whichever signal type was loudest in the past 60 days (e.g. enterprise escalations) and systematically under-weight quieter but more strategic signals (e.g. SMB churn). One quarter of skewed priorities and the roadmap drifts.

Mitigation: a hard 'evidence balance' eval gate - reject any priority list where less than 20% of cited sources come from any one source type. Run weekly; PM reviews.

## 6. V1 Scope

In: ranking the existing backlog with cited evidence; surfacing under-cited items; flagging conflicts between Slack escalations and Jira priorities.

Out: (1) hiring or headcount decisions, (2) customer-facing comms about why a feature was deprioritised. Both stay 100% with the human PM.
