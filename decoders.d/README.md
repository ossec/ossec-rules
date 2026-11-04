# Decoder fields

A decoder `name` is the string a rule uses in `<decoded_as>`, or the parent a child decoder attaches to. Child decoders pull fields out of one log line. The names below are the OSSEC fields these decoders fill.

| Field | Meaning |
| --- | --- |
| `location` | Where the log came from. Only on first-time-seen events. |
| `srcuser` | Source username. |
| `dstuser` | Target username. |
| `user` | Alias of `dstuser`. A decoder sets one of the two. |
| `srcip` | Source IP address. |
| `dstip` | Destination IP address. |
| `srcport` | Source port. |
| `dstport` | Destination port. |
| `protocol` | Protocol. |
| `id` | Event id. |
| `url` | URL on the event. |
| `action` | What the event did: deny, drop, accept, and similar. |
| `status` | Outcome: success, failure, and similar. |
| `extra_data` | Anything else the decoder captured. |

The full list of decoder names, and which file defines each one, is in [CATALOG.md](../CATALOG.md).
