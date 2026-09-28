# Storage Management

**STATUS: PROPOSED.** The WCM storage view unifies Windows-backed inventory, usage and supported management actions.

Show device-to-partition-to-volume relationships without conflating them; expose filesystem type, capacity/free space, mount points, health where supported, encryption state only through authorized APIs, and collection time. Separate physical device health from filesystem health. Offer safe cleanup recommendations only after estimating scope; deletion requires user selection and confirmation. Windows owns storage drivers, volume manager, filesystem implementation, caching and disk policy in the integrated phases. Operations can be unavailable due to edition, permissions, encryption, remote storage or device state.
