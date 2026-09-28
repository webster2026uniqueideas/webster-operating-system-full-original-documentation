# Groups

**STATUS: PROPOSED.** Windows local/domain groups and token memberships are authoritative for host permissions during integrated phases.

Webster may map capabilities to verified Windows identity/group information, subject to token and policy semantics. Group names are not stable authorization keys; use OS security identifiers and perform access checks at operation time. Webster application roles/preferences are separate namespaces and do not grant administrator authority. Display sensitive membership only to authorized viewers and do not cache it as timeless truth. Membership modification uses supported administration APIs and full audit/confirmation.
