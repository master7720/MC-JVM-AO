
| Category                  | Argument                       | Description |
|---------------------------|-------------------------------|-------------|
| Memory Allocation         | -Xmx4G                        | Sets the maximum amount of RAM Minecraft can use |
|          | -Xms2G                        | Sets the minimum amount of RAM Minecraft can use |
| Garbage Collector         | -XX:+UseG1GC                  | Enables the G1 garbage collector |
|          | -XX:MaxGCPauseMillis=200      | Tells the garbage collector to aim for pauses of no more than 200 milliseconds |
|          | -XX:+ParallelRefProcEnabled   | Allows reference processing to run in parallel during garbage collection |
|          | -XX:+DisableExplicitGC        | Prevents mods or the game from forcing full garbage collections |
|          | -Xlog:gc*:file=gc.log:time,uptime,level        | GC logging for diagnosing performance issues |
|          | -XX:+PrintGCDetails        | Prints detailed information about each GC event |
|          | -XX:+PrintGCDateStamps        | Adds timestamps to GC logs |
|          | -XX:+PrintGCApplicationStoppedTime        | Shows pauses caused by GC impacting Minecraft |
| G1GC Heap Tuning          | -XX:G1NewSizePercent=30       | Sets the minimum percentage of the heap used for new object allocation |
|           | -XX:G1MaxNewSizePercent=40    | Limits how large the young generation can grow |
|           | -XX:G1HeapRegionSize=8M       | Defines the size of G1GC memory regions |
|           | -XX:G1ReservePercent=20       | Keeps a portion of the heap in reserve to prevent allocation failures during sudden memory spikes |
|           | -XX:G1HeapWastePercent=5      | Controls how much unused space is tolerated in the heap before G1GC prioritizes cleanup |
| Survivor & Old Generation | -XX:SurvivorRatio=32          | Sets the ratio between Eden and Survivor spaces |
|  | -XX:MaxTenuringThreshold=1    | Causes objects to be promoted to the old generation quickly |
| Startup & Performance     | -XX:+UnlockExperimentalVMOptions | Allows the JVM to use advanced and experimental options |
|      | -XX:+AlwaysPreTouch            | Pre-allocates and touches all heap memory at startup |
|      | -XX:+PerfDisableSharedMem      | Disables JVM performance data sharing |
|      | -XX:+AlwaysActAsServerClassMachine | Forces the JVM to apply server-grade optimizations |
|      | -XX:+UseStringDeduplication | Deduplicates identical strings in memory |
| Compilation & JIT     | -XX:+TieredCompilation | Tiered JIT compilation for better runtime performance |
|      | -XX:+AggressiveOpts | Aggressive JVM optimizations |
|      | -XX:+OptimizeStringConcat | Faster string operations |
|      | -XX:CompileThreshold=1000 | Makes the JVM compile "hot" code faster |
| Native Memory & CPU     | -XX:+UseLargePages | May improve performance with large heaps (requires OS support) |
|      | -XX:ParallelGCThreads=16 | Use all cores for parallel GC(make sure to replace 16 with the actual number of physical cores your cpu has) |
|      | -XX:+UseNUMA | Optimizes memory on multi-socket CPUs |
|      | -XX:+UseCompressedOops | Saves memory on 64-bit JVM |
|      | -XX:+UseFastAccessorMethods | Improves method call performance for reflective calls |
| Misc     | -XX:+HeapDumpOnOutOfMemoryError | debugging mod memory leaks |
|      | -Dfile.encoding=UTF-8 | Ensures mods using text files work consistently |
|      | -Djava.net.preferIPv4Stack=true | can reduces network lag in multiplayer |



