# Solana Security Resources

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
- https://github.com/project-serum/sealevel-attacks/tree/master/programs
    - Tweet thread breakdown https://twitter.com/pencilflip/status/1483880018858201090
- [Neodyme Breakpoint Workshop](https://workshop.neodyme.io/)
    - CTF style!
- [Neodyme Breakpoint Workshop Video](https://www.youtube.com/watch?v=vbkhhgeP30I&ab_channel=Solana)
    - Goes over exercise 0 of Neodyme Breakpoint Workshop
- [Neodyme Solana Common Pitfalls](https://blog.neodyme.io/posts/solana_common_pitfalls)
    - Give hints to the Workshop exercises
- [Saber Library for basic security checks](https://github.com/saber-hq/vipers)
    - has asserts and other testing primitives. Some things are deprecated because automatically part of Anchor
- [Sencha account validators](https://github.com/SenchaHQ/sencha/blob/master/programs/cpamm/src/account_validators.rs)
    - Some account validation examples, uses vipers.
- [Assert Balances](https://github.com/project-serum/assert-balances)
    - Assertion instruction included on client-side/wallets, allows safe failure if unexpected result

# Hacks/Exploit reports
- [spl-token lending protocol exploit](https://blog.neodyme.io/posts/lending_disclosure)
- [Jet hack](https://medium.com/@0xjayne/-how-to-freely-borrow-all-the-tvl-from-the-jet-protocol-25d40e35920e)
- [Cope Pierre Hack](https://github.com/Arrowana/cope-roulette-pro)

# Contributing
- Please make any PR's or tweet at me for more additional resources/hack reports
