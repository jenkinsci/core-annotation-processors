This module defines an annotation processor that has the same name
as the one defined in core, to work around [MCOMPILER-97](https://issues.apache.org/jira/browse/MCOMPILER-97)

In this way, when javac tries to create an yet-compiled annotation processor, it will resolve to
this dummy definition, but since it's added to core as an optional dependency, when someone
actually depends on the jenkins core, it'll use the real processor defined in the core.
