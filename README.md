## Compilation / Usage

To setup our extension, run the following (assuming Linux):

```
git clone https://github.com/Bareflank/hypervisor
git clone https://github.com/boddumanohar/disable_lme.git
mkdir build; cd build
cmake ../hypervisor -DDEFAULT_VMM=example_vmm -DEXTENSION=../disable_lme
make -j<# cores + 1>
```

To test out our extended version of Bareflank, run the following commands:

```
make driver_quick
make quick
```

to get status information, use the following:

```
make status
make dump
```

to reverse this:

```
make unload
make driver_unload
```
