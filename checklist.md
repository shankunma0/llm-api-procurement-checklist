# Pre-signature checklist

Confirm every item in writing before signing. A verbal estimate is not a contractual commitment.

## 1. Models and versions

- Exact model names and versions.
- Context length.
- Required capabilities: tool calls, structured output, vision, or long context.
- Whether a version can be replaced by another model or version. Do not assume it can.

## 2. Billing items

Confirm pricing separately for:

- Input tokens.
- Output tokens.
- Cached input.
- Tool calls.
- Batch requests.
- Long-context requests.

A statement such as "about a percentage of the official price" is not enough to calculate the real cost.

## 3. Capacity limits

Record these separately:

- RPM: requests per minute.
- TPM: tokens per minute.
- Concurrent requests.

Enough capacity on one limit does not mean the other two are sufficient.

## 4. API compatibility

- Whether the target API and official SDK can be used directly.
- Differences in paths, parameters, error codes, and streaming.
- Compatibility does not mean every behavior matches the official API.

## 5. Data boundary

Confirm separately for the platform and each upstream model provider:

- Whether prompts, request content, and credentials are retained.
- How long they are retained.
- Whether they are used for training.
- Whether people can view them.

## 6. Failures and retries

- For HTTP 429, distinguish temporary rate limiting from billing or quota problems.
- Set a retry count, total time budget, and random delay.
- Prevent the SDK's automatic retries and the application's retries from stacking.

## 7. Timeouts and duplicate charges

- A client timeout does not prove that the server did not process the request.
- It also does not prove that the request was not billed.
- If partial streamed output or a tool action has already occurred, do not automatically rerun the entire task.

## 8. Support and responsibility

- Name the response owner.
- State the support hours and time zone.
- Define the escalation path.
- Automatic monitoring does not mean people are available all day.

Prices, capacity, data handling, and support terms are valid only when stated in a written quotation and contract.
