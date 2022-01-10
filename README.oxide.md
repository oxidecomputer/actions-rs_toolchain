## Oxide fork documentation

This project is a fork of [actions-rs/toolchain](https://github.com/actions-rs/toolchain).

### Justification

This fork was created to assist our efforts in enabling automatic pinning of our rust toolchain using renovate and the `rust-toolchain.toml` file. The upstream project only has support for the first version of the `rust-toolchain` file which is simply the toolchain version and nothing else. [actions-rs/toolchain#209](https://github.com/actions-rs/toolchain/pull/209) was created upstream to enable `toml` to be used in the `rust-toolchain` file as well as supporting the `.toml` extension. 

### When to delete this fork

After [actions-rs/toolchain#209](https://github.com/actions-rs/toolchain/pull/209) is merged upstream we may safely delete this fork and revert to using the upstream action. 

### Structure of the fork

Following our [🔒 recommended approach](https://github.com/oxidecomputer/rfd/tree/master/rfd/0211) this project uses `oxide/master` as it's main branch with the original projects `master` being preserved. Any changes to the project should be merged into `oxide/master` _not_ `master`. 

### Keeping the fork up-to-date

This project uses [wei/pull](https://github.com/wei/pull) to keep in sync with upstream changes. See `.github/pull.yml` for the relevant configuration. 
