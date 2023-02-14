<h1 align="center"><code> 🌬️:✝️:founly/f1 </code></h1>
<h2 align="center"><i> Founly edits and test 1</i></h2>

----
1. [Basket ?](#basket-)
2. [Dir Explanation](#dir-explanation)
3. [F1 - 1st Fuk](#f1---1st-fuk)
   1. [`cargo nextest run -v` - time](#cargo-nextest-run--v---time)
   2. [`cargo build --release` - time](#cargo-build---release---time)

----

# Basket ? 

1. Testing out founly editing for better or for worse 
2. Note compilation significantly slower in this free versions

# Dir Explanation 

F | DaF
|:--:|:--:|

# F1 - 1st Fuk 

Note waiting on the compilation tests which are being recorded [`here`](./banty/n1.txt) - Capturing the whole compilation output for later referencing

## `cargo nextest run -v` - time 

```js
flony1/f1 founly/f1*​ 12m51s 
```
- took about twice as long to compile 

## `cargo build --release` - time 

```rs
cargo build --release &> ../banty/b1.txt 
```

Note waiting on the compilation which occurs [`here`](./banty/b1.txt)
- Note you are getting this error 

```rs 
process didn't exit successfully: `rustc --crate-name foundry_evm --edition=2021 evm/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata,link -C opt-level=s -C panic=abort -C linker-plugin-lto -C codegen-units=1 -C debuginfo=0 -C metadata=3ee26b3925534395 -C extra-filename=-3ee26b3925534395 --out-dir /workspaces/flony1/f1/target/release/deps -C strip=symbols -L dependency=/workspaces/flony1/f1/target/release/deps --extern auto_impl=/workspaces/flony1/f1/target/release/deps/libauto_impl-ee8789e45f41d01e.so --extern bytes=/workspaces/flony1/f1/target/release/deps/libbytes-9d19b62ca5edbbbd.rmeta --extern ethers=/workspaces/flony1/f1/target/release/deps/libethers-38b6e44d37becacf.rmeta --extern eyre=/workspaces/flony1/f1/target/release/deps/libeyre-165af892341f9fac.rmeta --extern foundry_common=/workspaces/flony1/f1/target/release/deps/libfoundry_common-1ac37b731d260add.rmeta --extern foundry_config=/workspaces/flony1/f1/target/release/deps/libfoundry_config-31f4582d87422308.rmeta --extern foundry_macros=/workspaces/flony1/f1/target/release/deps/libfoundry_macros-e39f64580b8b6d52.rmeta --extern futures=/workspaces/flony1/f1/target/release/deps/libfutures-1ae50cde159cda02.rmeta --extern hashbrown=/workspaces/flony1/f1/target/release/deps/libhashbrown-9a09214b8d7a37c8.rmeta --extern hex=/workspaces/flony1/f1/target/release/deps/libhex-b3636f499f629989.rmeta --extern itertools=/workspaces/flony1/f1/target/release/deps/libitertools-71ad8a32c3232199.rmeta --extern jsonpath_lib=/workspaces/flony1/f1/target/release/deps/libjsonpath_lib-40ae717dafb92f93.rlib --extern once_cell=/workspaces/flony1/f1/target/release/deps/libonce_cell-a61683508615d138.rmeta --extern ordered_float=/workspaces/flony1/f1/target/release/deps/libordered_float-e99b7303a8f0ee39.rmeta --extern parking_lot=/workspaces/flony1/f1/target/release/deps/libparking_lot-e2250ee5d638d38b.rmeta --extern proptest=/workspaces/flony1/f1/target/release/deps/libproptest-1fbbab70deac8942.rmeta --extern revm=/workspaces/flony1/f1/target/release/deps/librevm-f703805a63845e96.rmeta --extern semver=/workspaces/flony1/f1/target/release/deps/libsemver-35306dbe8f075bcd.rmeta --extern serde=/workspaces/flony1/f1/target/release/deps/libserde-433c07677b486297.rmeta --extern serde_json=/workspaces/flony1/f1/target/release/deps/libserde_json-e461003c0b18d075.rmeta --extern thiserror=/workspaces/flony1/f1/target/release/deps/libthiserror-b10a84c0c01dae67.rmeta --extern tokio=/workspaces/flony1/f1/target/release/deps/libtokio-32c642b81aff788f.rmeta --extern tracing=/workspaces/flony1/f1/target/release/deps/libtracing-86b4084f2e53ea82.rmeta --extern url=/workspaces/flony1/f1/target/release/deps/liburl-c29ba939eba6250f.rmeta --extern yansi=/workspaces/flony1/f1/target/release/deps/libyansi-7cfa1b16a877f83e.rmeta -L native=/workspaces/flony1/f1/target/release/build/ring-3f3f3411d111fd21/out -L native=/workspaces/flony1/f1/target/release/build/hidapi-rusb-17bdc046f1b7ba88/out -L native=/workspaces/flony1/f1/target/release/build/libusb1-sys-32d6d7100ae780da/out -L native=/workspaces/flony1/f1/target/release/build/secp256k1-sys-83b7e70b6ca3be87/out` (signal: 9, SIGKILL: kill)

# Part important from this is 
signal: 9, SIGKILL: kill 
- This shit has a memory issue need to bump the instance


```