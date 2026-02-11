# Description

This is a quick demonstration of how lerna version is broken.

## Getting Started

```sh
git clone https://github.com/anthony-bonta-gaf-energy/gafe-lerna-test.git
cd gafe-lerna-test
yarn install
```

## Repro steps

* Create any change in packages/package-a
* Commit the changes with the comment "docs!: did some update"
* Run

```sh
yarn bump
```

## Expected results

The major version is updated from 5.0.10 to 6.0.0

## Actual Results

The version is updated to 5.0.11

## Additional Notes

Not only is the major version not updating, if you just use feat: or feature:, that seems to have stopped working as well.  Only patch seems to work.