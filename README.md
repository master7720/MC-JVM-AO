
| Category                  | Argument                       | Description |
|---------------------------|-------------------------------|-------------|
| Memory Allocation         | -Xmx4G                        | Sets the maximum amount of RAM Minecraft can use |
|                           | -Xms2G                        | Sets the minimum amount of RAM Minecraft can use |
| Garbage Collector         | -XX:+UseG1GC                  | Enables the G1 garbage collector |
|                           | -XX:MaxGCPauseMillis=200      | Tells the garbage collector to aim for pauses of no more than 200 milliseconds |
|                           | -XX:+ParallelRefProcEnabled   | Allows reference processing to run in parallel during garbage collection |
|                           | -XX:+DisableExplicitGC        | Prevents mods or the game from forcing full garbage collections |
|                           | -Xlog:gc*:file=gc.log:time,uptime,level | GC logging for diagnosing performance issues |
|                           | -XX:+PrintGCDetails           | Prints detailed information about each GC event |
|                           | -XX:+PrintGCDateStamps        | Adds timestamps to GC logs |
|                           | -XX:+PrintGCApplicationStoppedTime | Shows pauses caused by GC impacting Minecraft |
| G1GC Heap Tuning          | -XX:G1NewSizePercent=30       | Sets the minimum percentage of the heap used for new object allocation |
|                           | -XX:G1MaxNewSizePercent=40    | Limits how large the young generation can grow |
|                           | -XX:G1HeapRegionSize=8M       | Defines the size of G1GC memory regions |
|                           | -XX:G1ReservePercent=20       | Keeps a portion of the heap in reserve to prevent allocation failures during sudden memory spikes |
|                           | -XX:G1HeapWastePercent=5      | Controls how much unused space is tolerated in the heap before G1GC prioritizes cleanup |
| Survivor & Old Generation | -XX:SurvivorRatio=32          | Sets the ratio between Eden and Survivor spaces |
|                           | -XX:MaxTenuringThreshold=1    | Causes objects to be promoted to the old generation quickly |
| Startup & Performance     | -XX:+UnlockExperimentalVMOptions | Allows the JVM to use advanced and experimental options |
|                           | -XX:+UnlockDiagnosticVMOptions | Allows access to additional JVM diagnostic options |
|                           | -XX:+AlwaysPreTouch           | Pre-allocates and touches all heap memory at startup |
|                           | -XX:+PerfDisableSharedMem     | Disables JVM performance data sharing |
|                           | -XX:+AlwaysActAsServerClassMachine | Forces the JVM to apply server-grade optimizations |
|                           | -XX:+UseStringDeduplication   | Deduplicates identical strings in memory |
| Compilation & JIT         | -XX:+TieredCompilation        | Tiered JIT compilation for better runtime performance |
|                           | -XX:+AggressiveOpts           | Aggressive JVM optimizations |
|                           | -XX:+OptimizeStringConcat     | Faster string operations |
|                           | -XX:CompileThreshold=1000     | Makes the JVM compile "hot" code faster |
|                           | -XX:NmethodSweepActivity=1   | Controls JIT code cache sweeps to manage compiled code |
|                           | -XX:ReservedCodeCacheSize=400M | Sets max size of JIT code cache |
|                           | -XX:NonNMethodCodeHeapSize=12M | Sets size for non-method code heap |
|                           | -XX:ProfiledCodeHeapSize=194M | Sets size of code heap for profiled methods |
|                           | -XX:NonProfiledCodeHeapSize=194M | Sets size of code heap for non-profiled methods |
|                           | -XX:-DontCompileHugeMethods   | Allows compilation of very large methods |
|                           | -XX:MaxNodeLimit=240000       | JIT compiler internal limit for code nodes |
|                           | -XX:NodeLimitFudgeFactor=8000 | JIT compiler tuning factor for node limits |
| Native Memory & CPU       | -XX:+UseLargePages            | May improve performance with large heaps (requires OS support) |
|                           | -XX:ParallelGCThreads=16      | Use all cores for parallel GC (replace 16 with your CPU cores) |
|                           | -XX:+UseNUMA                  | Optimizes memory on multi-socket CPUs |
|                           | -XX:+UseCompressedOops        | Saves memory on 64-bit JVM |
|                           | -XX:+UseFastAccessorMethods   | Improves method call performance for reflective calls |
|                           | -XX:+UseVectorCmov            | CPU optimization for vectorized conditional moves |
|                           | -XX:+UseFastUnorderedTimeStamps | Performance optimization for timestamps |
|                           | -XX:+UseCriticalJavaThreadPriority | Uses OS thread priority for critical Java threads |
|                           | -XX:ThreadPriorityPolicy=1    | Controls how JVM threads apply OS thread priorities |
|                           | -XX:+AllocatePrefetchStyle=3  | Memory prefetching optimization for allocation |
| Misc                      | -XX:+HeapDumpOnOutOfMemoryError | Dumps memory on OOM errors for debugging |
|                           | -Dfile.encoding=UTF-8         | Ensures mods using text files work consistently |
|                           | -Djava.net.preferIPv4Stack=true | Can reduce network lag in multiplayer |
