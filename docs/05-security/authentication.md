# Authentication

**STATUS: PROPOSED.** In the Windows-integrated phases, Windows authenticates interactive users and provides the process token. Webster consumes the OS-provided identity; it does not establish a parallel password authority by default.

Webster may require reauthentication/consent for sensitive workflows by invoking supported Windows mechanisms. It must not collect or cache Windows passwords, imitate the Windows secure desktop, or accept UI claims as proof of identity. Authenticator availability (local, domain, Microsoft Entra or other managed configuration) is Windows/policy dependent. Future independent-OS authentication is **FUTURE / RESEARCH** and requires a separate credential, recovery and threat design.
