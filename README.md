# require addgroup

```
[export ADDGROUP_GID=<number>]
[export ADDGROUP_GIDFORCE=<number>]
[export ADDGROUP_NAME=<string>]
require addgroup [groupname]
```

Ensure that named group existsin a system.  Either environment variable
`ADDGROUP_NAME` or an argument `groupname` must be prvovided.

If `ADDGROUP_GIDFORCE` is provided, module fails if group already exists
with different gid.

If `ADDGROUP_GID` is set, creation of the group prefers this gid for
the newly created group. If unset, defaults to `ADDGROUP_GIDFORCE`.

Obsolete `GROUP_GID` and `GROUP_NAME` are defaults accepted at least until
end of 2023 and will be removed afterwards.
