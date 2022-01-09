# Changelog

`hedgehog-classes` uses [PVP Versioning][1].
The changelog is available [on GitHub][2].

Unreleased
=======
* Make `Hedgehog.Classes.Aeson` module empty when the `aeson` flag is disabled.
* Make `Hedgehog.Classes.Prim` module empty when the `primitive` flag is disabled.

0.2.5.3
=======
* Correct bug in which `storablePeekByte` uses the wrong offset values
* Update base upper bound. [4.12, 4.15) -> [4.12, 4.17)
* Update semirings upper bound. [0.2, 0.7) -> [0.2, 0.8)
* Update aeson upper bound. [0.9, 1.6) -> [0.9, 2.1)

0.2.5.2
=======
* Update semirings upper bound. [0.2, 0.6) -> [0.2, 0.7)

0.2.5.1
=======
* Bump upper bound on pretty-show from <1.10 to <1.11

0.2.5
=====
* Add MUVector laws
* Update upper bounds on dependencies

0.2.4.1
=======
* Fix error introduced by change of hedgehog's
  internal API between hedgehog-1.0.1 and
  hedgehog-1.0.2.
* Re-add GHC 8.8.1 to cabal's tested-with field.

0.2.4
=====
* Semirings upper bound increased to 0.6. [0.2, 0.5) -> [0.2, 0.6)
* Add `primLaws`.
* Remove GHC 8.8.1 from cabal's tested-with field.
* Add documentation to `comonadLaws`.

0.2.3
=====
* Semirings upper bound increased to 0.5. Lower bound not touched.
  [0.2, 0.4) -> [0.2, 0.5)
* Add `comonadLaws`.

0.2.2
=====
* fix problem in storable set-get that caused attempt to index into
  0-element malloc'd array
* Test suite now tests almost all laws sans arrow/category (thanks @ag-eitilt!)
* Correct tcName of `MonadPlus`. Was `Monad`, now it's `MonadPlus`.

0.2.1
=====
* fix problem where ordLaws failed for everything. there was
  some messed up logic used to check that transitivity held.
  Thanks very much to @ocharles for reporting this.

0.2.0.1
=======
* improve reliability of hedgehog output filtering.

0.2
===
* switch to hedgehog-1.0
* add `binaryLaws`
* relax cabal-version to 2.2
* use randomly generated, not hard-coded functions, in bifoldable tests
* significantly simplify pretty printing using `silently` package, and
  bad hack.
* make several haddock improvements.

0.1.2
=====

* add `semiringLaws`, `ringLaws`, `starLaws`
* fix bug in `foldableLaws` that could cause implementations of
  `foldMap` and `fold` that evaluate in weird orders to pass (rather than fail).

0.1.1
=====

* Initial (stable) hackage release.

0.0.0
=====

* Initially created.

[1]: https://pvp.haskell.org
[2]: https://github.com/chessai/hedgehog-classes/releases
