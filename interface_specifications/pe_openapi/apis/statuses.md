# Status

A presentation exchange can be in a different states. In (roughly) each state we can define what is the status by following:

* `status` can contain the following values:
  * `CREATED`: create a session http request was successful
  * `SUBMITTED`: Holder responded with a presentation
  * `HOLDER_DECLINED`: (holder_refused)Holder explicitly declined, Holder called some API to update the status.
  * `EXPIRED`: Holder did not respond at all or did not respond in time.
  * `ACCEPTED`: (completed/verified/valid/approved) Presentation was accepted by the verifier.
  * `VERIFIER_DECLINED`: (verifier_rejected) Presentation was rejected by verifier