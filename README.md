# GitHub Action - Run tests
Run Silverstripe CI matrix tests

Only intended to be used within [gha-ci](https://github.com/silverstripe/gha-ci). The inputs all come from the matrix generated as a part of that workflow.

GitHub job permissions required: `none`

## JS license checking

This action will check the licences of any installed NPM dependencies against a list of allowed SPDX identifiers of open source licences. These are contained in semi-colon delimited list in `allowed-spdx-delimited.txt`. If any insalaled non-dev dependencies are found that are not in the allowed list then the job will fail. See https://spdx.org/licenses/ for a list of SPDX identifiers.

Note that the `Unlicense` is an SPDX identifier for an actual license and not a placeholder for a missing license.

Composer dependences are checked seperately in `ci.yml` of `silverstripe/recipe-kitchen-sink`.
