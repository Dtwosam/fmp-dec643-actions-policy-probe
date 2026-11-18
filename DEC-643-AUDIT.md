# DEC-643 Actions policy probe

Disposable repository only. This file does not change FMP.

## Identity

- Repository: `Dtwosam/fmp-dec643-actions-policy-probe` (id `1462609624`)
- Public, owner type User, owner `Dtwosam` (id `42391449`)
- Default branch commit at dispatch: `7a54820f75994c40cbbac69e8748d63795f1fa15`
- Workflow: `.github/workflows/dec643-dispatch-probe.yml`
- Workflow id: `422429578`
- Workflow state at test: active
- Secrets, hooks, deploy keys: 0
- Other workflows: 0

## Policy

- Id `15774`, name `DEC-643 deny workflow_dispatch`
- Enforcement: `active`
- Workflow path include: `.github/workflows/dec643-dispatch-probe.yml`
- Rule: `restrict_action_events`, `allowed_events: ["push"]`
- `workflow_dispatch` was not an allowed event
- Read back through `GET /repos/Dtwosam/fmp-dec643-actions-policy-probe/actions/policies/15774` before the dispatch
- API version used for the policy and the dispatch: `2026-03-10`
- Policy deleted after the test. Delete response: HTTP 204. Subsequent policy list `total_count` 0.

## Baseline

- Workflow run `total_count`: 0
- Maximum run number: none

## Single dispatch

- `POST /repos/Dtwosam/fmp-dec643-actions-policy-probe/actions/workflows/422429578/dispatches`
- Body field: `ref=main`
- Caller: `Dtwosam`
- Response: HTTP 200
- Body: `workflow_run_id` `44280537666`
- No retry

## Run created

- Id: `44280537666`
- Run number: 1
- Attempt: 1
- Event: `workflow_dispatch`
- Status: `completed`
- Conclusion: `startup_failure`
- Head: `7a54820f75994c40cbbac69e8748d63795f1fa15`
- Jobs: 0
- Annotation: Event 'workflow_dispatch' is not allowed to trigger Actions workflows. Workflow file: '.github/workflows/dec643-dispatch-probe.yml'.
- Post-request workflow run `total_count`: 1
- Maximum run number: 1

## Verdict

`BLOCKED_RUN_ALLOCATED`

The repository is retained. Deletion was not authorized.
