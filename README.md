# hello-world
just another repository
// This interface will compile into required Wasm imports.
// A complete documentation those functions is available in the VM that provides them:
// https://github.com/CosmWasm/cosmwasm/blob/0.7/lib/vm/src/instance.rs#L43
//
// TODO: use feature switches to enable precompile dependencies in the future,
// so contracts that need less
extern "C" {
    fn read_db(key: *const c_void, value: *mut c_void) -> i32;
    fn write_db(key: *const c_void, value: *mut c_void);
    fn canonicalize_address(human: *const c_void, canonical: *mut c_void) -> i32;
    fn humanize_address(canonical: *const c_void, human: *mut c_void) -> i32;
}
