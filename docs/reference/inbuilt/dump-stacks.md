# SYS.DUMP_STACKS

Writes thread stacks, locks, and transaction states to the SnappyData log file. You can write stack information either for the current SnappyData member or for all SnappyData members in the distributed system.

See also <a href="../store_commands/store-print-stacks.html#reference_13F8B5AFCD9049E380715D2EF0E33BDC" class="xref" title="Prints a stack dump of SnappyData member processes.">print-stacks</a> for information about writing thread stacks to standard out or to a specified file.

##Syntax

``` pre
SYS.DUMP_STACKS (
IN ALL BOOLEAN
)
```

**ALL**   
Specifies boolean value: "true" to log stack trace information for all SnappyData members, or "false" to log information only for the local SnappyData member.

##Example

This command writes thread stack information only for the local SnappyData member. The stack information is written to the SnappyData log file (by default <span class="ph filepath">gfxdserver.log</span> in the member startup directory):

``` pre
snappy> call sys.dump_stacks('false');
Statement executed.
```

See <a href="../store_commands/store-print-stacks.html#reference_13F8B5AFCD9049E380715D2EF0E33BDC" class="xref" title="Prints a stack dump of SnappyData member processes.">print-stacks</a> for an example of the partial thread stack output.

