# Modules

## Names

Modules should use snake case names e.g. my_module_name.

## File Organization

If a module contains sub-modules, each of these sub-modules should be placed in its own file. The one exception to this rule is test modules. If they are reasonably short, it may make more sense to include them in the module they are testing.

Now, for an example. Say the module layout is as follows:

```
m1
|-m11
|-m12
  |-m121
  |-m122
    |-m1221
  |-m123
|-m13
  |-m131
|-m14
m2
```

The file layout should then be this:

```
m1
|-mod.rs
|-m11.rs
|-m12
  |-mod.rs
  |-m121.rs
  |-m122
    |-mod.rs
    |-m1221.rs
  |-m123.rs
|-m13
  |-mod.rs
  |-m131.rs
|-m14.rs
m2.rs
```
