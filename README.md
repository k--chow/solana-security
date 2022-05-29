# Solana Security Resources
- [Osec's guide to an auditor's introduction](https://osec.io/blog/tutorials/2022-03-14-solana-security-intro/)
- [Solend Auditing Workshop](https://docs.google.com/presentation/d/1jZ9kVo6hnhBsz3D2sywqpMojqLE5VTZtaXna7OHL1Uk/edit?pli=1#slide=id.ge15c343642_0_51)
    - more general blockchain than solana-specific

- Soteria Series on Auditing
    - [Intro](https://medium.com/coinmonks/how-to-audit-solana-smart-contracts-part-1-a-systematic-approach-56a434f6c-9ed)
    - [Scanning Tools](https://medium.com/coinmonks/how-to-audit-solana-smart-contracts-part-2-automated-scanning-ceb88830ae6d)
    - [Penetration Testing](https://medium.com/coinmonks/how-to-audit-solana-smart-contracts-part-3-penetration-testing-a315b3bbb2d3)
    - [Anchor](https://medium.com/coinmonks/how-to-audit-solana-smart-contracts-part-4-the-anchor-framework-ef42d944f086)
- [Soteria blog](https://blog.soteria.dev/?p=ceb88830ae6d)
- [Soldev compilation of security resources](https://www.soldev.app/library/security/dfrMbk07g)
- [Kudelski Solana Security Part 1](https://research.kudelskisecurity.com/2021/09/15/solana-program-security-part1/)
- Armani Tweets about security
    - https://twitter.com/armaniferrante/status/1411589639006154754?s=21
    - https://twitter.com/armaniferrante/status/1411589629384355840?s=21
        - Archive (in case of deadlink): https://threadreaderapp.com/thread/1411589629384355840.html
- [Sealevel attacks by Armani](https://github.com/project-serum/sealevel-attacks/tree/master/programs)
    - Common malpractices (broken into secure, insecure, recommended)
    - Tweet thread breakdown https://twitter.com/pencilflip/status/1483880018858201090
- [Neodyme Solana Common Pitfalls](https://blog.neodyme.io/posts/solana_common_pitfalls)
    - Give hints to the Workshop exercises
- [Saber Library for basic security checks](https://github.com/saber-hq/vipers)
    - has asserts and other testing primitives. Some things are deprecated because automatically part of Anchor
- [Sencha account validators](https://github.com/SenchaHQ/sencha/blob/master/programs/cpamm/src/account_validators.rs)
    - Some account validation examples, uses vipers.
- [Assert Balances](https://github.com/project-serum/assert-balances)
    - Assertion instruction included on client-side/wallets, allows safe failure if unexpected result

- Soteria Series on Internals
    - [Part 1: On chain programs](https://www.soteria.dev/post/solana-internals-part-1-what-are-the-native-on-chain-programs-and-why-do-they-matter)
    - [Part 2: Deploying and upgrading under the hood](https://www.soteria.dev/post/solana-internals-part-2-how-is-a-solana-program-deployed-and-upgraded)
    - [Part 3: How the Transaction Processing Unit works](https://www.soteria.dev/post/solana-internals-part-3-the-transaction-processing-unit-tpu)
    - [Part 4: Bank Internals](https://www.soteria.dev/post/solana-internals-part-4-the-bank-a-key-component)
## Hands On (CTF Challenges)
- [Neodyme Breakpoint Workshop](https://workshop.neodyme.io/)
    - CTF style
- [Neodyme Breakpoint Workshop Video](https://www.youtube.com/watch?v=vbkhhgeP30I&ab_channel=Solana)
    - Goes over exercise 0 of Neodyme Breakpoint Workshop
- [TJCTF 2022 Moar-Horse-5](https://ctf.tjctf.org/)
    - CTF Solana challenge
- [PicoCTF 2022 Solfire](https://play.picoctf.org/practice?page=1&search=solfire)
    - CTF Solana challenge


# Hacks/Bug bounty reports
- [spl-token lending protocol exploit (neodyme)](https://blog.neodyme.io/posts/lending_disclosure)
- [spl-token-swap rounding exploit (osec)](https://osec.io/blog/reports/2022-04-26-spl-swap-rounding/)
    - [Osec tweet](https://twitter.com/osec_io/status/1518967950610362368)
- [Jet hack](https://medium.com/@0xjayne/-how-to-freely-borrow-all-the-tvl-from-the-jet-protocol-25d40e35920e)
- [Cope Pierre Hack](https://github.com/Arrowana/cope-roulette-pro)
- [Wallet simulation rug pull](https://opcodes.fr/publications/2022-01/detecting-transaction-simulation/)
    - [Tweet about it](https://twitter.com/TheCryptoBird/status/1488560566029500427?s=20&t=l9rpVewzESNoByVd0MPe1g)
- [Why Magic Eden is garbage Tweet](https://twitter.com/AndreiBalici/status/1488077648542769154?s=20&t=l9rpVewzESNoByVd0MPe1g)
    - transferring token authority from user to magic eden
    - https://github.com/solana-labs/solana-program-library/issues/2640
- [Wormhole Hack](https://twitter.com/samczsun/status/1489044939732406275)
    - call complete_wrapped (instruction 03)
    - post_VAA (instruction 02) called on main bridge
    - `solana_program::sysvar::instructions` not verified in this vesion of solana_program
    - https://twitter.com/wireless_anon/status/1489075372662476800?s=20&t=XHV8n8c4DJOBzcKwzAqunw
    - unmerged PR to fix issue: https://github.com/certusone/wormhole/commit/7edbbd3677ee6ca681be8722a607bc576a3912c8#diff-0d27d8889edd071b86d3f3299276882d97613ad6ab3b0b6412ae4ebf3ccd6370L92-R101
- [Soteria Bug report on solana stake pool](https://medium.com/coinmonks/solana-stake-pool-a-semantic-inconsistency-vulnerability-discovered-by-soteria-b92abcbaf909)
- [Potential Solana attack vector on ERC-20 approve (Actually happened to Solfire victims)](https://2501babe.github.io/tools/revoken.html)
- [exchgART hack](https://twitter.com/exchgART/status/1489881735642947589?s=20&t=SDiPEXeh3SjfCyOv7zXaBg)
    - [Archive thread](https://threadreaderapp.com/thread/1489881735642947589.html)
    - drained funds in offer accounts. But refunded.
- [Jet 20m bug report](https://www.jetprotocol.io/posts/jet-bug-disclosure)
    - [Tweet breakdown](https://twitter.com/charlieyouai/status/1508842093514567687?s=21&t=GhJJPq1QvKut5JIU8he9Uw)
- [Serum v4 bug](https://forum.projectserum.com/t/bug-bounty-for-loss-of-funds-bug-in-aob/446)
- [Serum Zero day](https://www.btblock.io/post/btblock-finds-serum-zero-day-serum-fixes-immediately)
- [Cashio hack (Soteria)](https://www.soteria.dev/post/cashioapp-attack-whats-the-vulnerability-and-how-soteria-detects-it)
- [Cheating Oracles on Solana](https://osec.io/blog/reports/2022-02-16-lp-token-oracle-manipulation/)
- [Integer overflow in rBPF](https://blocksecteam.medium.com/new-integer-overflow-bug-discovered-in-solana-rbpf-7729717159ee)

# Contributing
- Please make any PR's or tweet @kevinchow23 for more additional resources/hack reports
- Internet archive posts + tweets
