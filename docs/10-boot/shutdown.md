# Shutdown

**STATUS: PROPOSED.** Webster shutdown means orderly closure of its processes; Windows owns machine shutdown/restart.

Stop accepting new work, cancel or finish bounded operations, flush documented user state/audit records, close handles and exit within a deadline. Do not block Windows logoff or claim system power-off. Pending privileged operations report complete, canceled or uncertain state. If the user invokes shutdown/restart, Webster follows Windows session notifications and avoids conflicting prompts. Future standalone OS power sequencing is **FUTURE / RESEARCH**.
