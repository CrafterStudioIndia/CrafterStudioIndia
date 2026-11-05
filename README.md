---- Minecraft Crash Report ----
// You're mean.

Time: 2026-11-05 19:49:37
Description: Initializing game

java.lang.RuntimeException: Could not execute entrypoint stage 'client' due to errors, provided by 'nodelay' at 'org.swag.nodelay.client.NodelayClient'!
	at net.fabricmc.loader.impl.FabricLoaderImpl.lambda$invokeEntrypoints$0(FabricLoaderImpl.java:418)
	at net.fabricmc.loader.impl.util.ExceptionUtil.gatherExceptions(ExceptionUtil.java:33)
	at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:416)
	at net.fabricmc.loader.impl.game.minecraft.Hooks.startClient(Hooks.java:53)
	at knot//net.minecraft.client.Minecraft.<init>(Minecraft.java:456)
	at knot//net.minecraft.client.main.Main.main(Main.java:278)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:517)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:72)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)
Caused by: java.lang.NoClassDefFoundError: net/minecraft/class_2561
	at knot//org.swag.nodelay.client.NodelayClient.onInitializeClient(NodelayClient.java:23)
	at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:414)
	... 6 more
Caused by: java.lang.ClassNotFoundException: net.minecraft.class_2561
	at java.base/jdk.internal.loader.BuiltinClassLoader.loadClass(BuiltinClassLoader.java:580)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:490)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.loadClass(KnotClassDelegate.java:240)
	at net.fabricmc.loader.impl.launch.knot.KnotClassLoader.loadClass(KnotClassLoader.java:119)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:490)
	... 8 more


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Render thread
Stacktrace:
	at net.fabricmc.loader.impl.FabricLoaderImpl.lambda$invokeEntrypoints$0(FabricLoaderImpl.java:418)
	at net.fabricmc.loader.impl.util.ExceptionUtil.gatherExceptions(ExceptionUtil.java:33)
	at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:416)
	at net.fabricmc.loader.impl.game.minecraft.Hooks.startClient(Hooks.java:53)
	at knot//net.minecraft.client.Minecraft.<init>(Minecraft.java:456)

-- Initialization --
Details:
	Modules: 
Stacktrace:
	at knot//net.minecraft.client.main.Main.main(Main.java:278)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:517)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:72)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)

-- System Details --
Details:
	Minecraft Version: 26.2
	Minecraft Version ID: 26.2
	Operating System: Linux (amd64) version 7.3.1-1-cachyos
	Java Version: 25.0.5.0.3, Arch Linux
	Java VM Version: OpenJDK 64-Bit Server VM (mixed mode, sharing), Arch Linux
	Memory: 3503308384 bytes (3341 MiB) / 4294967296 bytes (4096 MiB) up to 4294967296 bytes (4096 MiB)
	Memory (heap): init: 4096MiB, used: 746MiB, committed: 4096MiB, max: 4096MiB
	Memory (non-head): init: 007MiB, used: 150MiB, committed: 152MiB, max: 000MiB
	CPUs: 16
	Processor Vendor: GenuineIntel
	Processor Name: 12th Gen Intel(R) Core(TM) i7-12650H
	Identifier: Intel64 Family 6 Model 154 Stepping 3
	Microarchitecture: Alder Lake
	Frequency (GHz): -0.00
	Number of physical packages: 1
	Number of physical CPUs: 10
	Number of logical CPUs: 16
	Graphics card #0 name: Alder Lake-P GT1 [UHD Graphics]
	Graphics card #0 vendor: Intel Corporation (0x8086)
	Graphics card #0 VRAM (MiB): 256.00
	Graphics card #0 deviceId: 0x46a3
	Graphics card #0 versionInfo: unknown
	Graphics card #1 name: AD106M [GeForce RTX 3050 A Laptop GPU]
	Graphics card #1 vendor: NVIDIA Corporation (0x10de)
	Graphics card #1 VRAM (MiB): 4128.00
	Graphics card #1 deviceId: 0x2822
	Graphics card #1 versionInfo: unknown
	Virtual memory max (MiB): 39809.93
	Virtual memory used (MiB): 14133.95
	Swap memory total (MiB): 32000.99
	Swap memory used (MiB): 4803.98
	Space in storage for jna.tmpdir (MiB): available: 148826.67, total: 314195.00
	Space in storage for org.lwjgl.system.SharedLibraryExtractPath (MiB): available: 148826.67, total: 314195.00
	Space in storage for io.netty.native.workdir (MiB): available: 148826.67, total: 314195.00
	Space in storage for java.io.tmpdir (MiB): available: 7705.57, total: 7808.93
	Space in storage for workdir (MiB): available: 148826.67, total: 314195.00
	Operating System Version: GNU/Linux Arch Linux unknown (unknown) build 7.3.1-1-cachyos
	Process Elevated: false
	Process Loads: Uptime: 7s, user: 23s (316.35%), kernel: 1s (11.08%), total: 24s (327.43%)
	Process Virtual Size (MiB): 6878.32
	Process Resident Size (MiB): 1384.84
	JVM Flags: 16 total; -Xmx4096M -Xms4096M -XX:+UseG1GC -XX:+UnlockExperimentalVMOptions -XX:MaxGCPauseMillis=37 -XX:+ParallelRefProcEnabled -XX:+DisableExplicitGC -XX:G1NewSizePercent=23 -XX:G1MaxNewSizePercent=50 -XX:G1HeapRegionSize=16M -XX:G1ReservePercent=20 -XX:InitiatingHeapOccupancyPercent=20 -XX:G1MixedGCCountTarget=3 -XX:+PerfDisableSharedMem -XX:+UseStringDeduplication -XX:+UseCompactObjectHeaders
	Debug Flags: 0 total; 
	Fabric Mods: 
		badoptimizations: BadOptimizations 2.4.1
		chat_heads: Chat Heads 1.3.2
		cloth-config: Cloth Config v26.2 26.2.155
			cloth-basic-math: cloth-basic-math 0.6.1
		elytra-chestplate-swapper: Elytra Chestplate Swapper 2.1.0
		entityculling: EntityCulling 1.11.3
			transition: TRansition 1.0.26
			trender: TRender 1.0.17
		fabric-api: Fabric API 0.161.0+26.2
			fabric-advancement-api-v1: Fabric Advancement API (v1) 1.0.0+58719a3b9e
			fabric-api-base: Fabric API Base 2.0.4+ece063239e
			fabric-api-lookup-api-v1: Fabric API Lookup API (v1) 2.0.18+11e1c9a39e
			fabric-biome-api-v1: Fabric Biome API (v1) 18.0.6+c7bd5b8e9e
			fabric-block-api-v1: Fabric Block API (v1) 3.1.0+53515aab9e
			fabric-block-getter-api-v2: Fabric BlockGetter API (v2) 2.0.7+ec56b6019e
			fabric-command-api-v2: Fabric Command API (v2) 3.1.0+00cb03469e
			fabric-content-registries-v0: Fabric Content Registries (v0) 11.3.2+37b1aa249e
			fabric-convention-tags-v2: Fabric Convention Tags (v2) 4.7.1+1f023a9e9e
			fabric-crash-report-info-v1: Fabric Crash Report Info (v1) 1.0.5+086d547a9e
			fabric-creative-tab-api-v1: Fabric Creative Tab API (v1) 5.0.15+6468574f9e
			fabric-data-attachment-api-v1: Fabric Data Attachment API (v1) 2.2.19+515ac5339e
			fabric-data-generation-api-v1: Fabric Data Generation API (v1) 25.6.0+c0da0b829e
			fabric-debug-api-v1: Fabric Debug API (v1) 1.0.2+c792624d9e
			fabric-dimensions-v1: Fabric Dimensions API (v1) 5.1.12+515ac5339e
			fabric-entity-events-v1: Fabric Entity Events (v1) 5.0.5+06488ac19e
			fabric-events-interaction-v0: Fabric Events Interaction (v0) 5.2.8+515ac5339e
			fabric-game-rule-api-v1: Fabric Game Rule API (v1) 4.0.8+46a6d00c9e
			fabric-item-api-v1: Fabric Item API (v1) 14.5.0+c68f6cbe9e
			fabric-key-mapping-api-v1: Fabric Key Mapping API (v1) 2.0.5+e2bdee789e
			fabric-lifecycle-events-v1: Fabric Lifecycle Events (v1) 4.1.4+29b6eb019e
			fabric-loot-api-v3: Fabric Loot API (v3) 3.0.17+06488ac19e
			fabric-menu-api-v1: Fabric Menu API (v1) 2.0.17+086d547a9e
			fabric-message-api-v1: Fabric Message API (v1) 7.0.8+bb2ed3f79e
			fabric-model-loading-api-v1: Fabric Model Loading API (v1) 8.0.17+c80601bb9e
			fabric-networking-api-v1: Fabric Networking API (v1) 6.3.4+2989c6a09e
			fabric-object-builder-api-v1: Fabric Object Builder API (v1) 24.1.1+6fcd5f039e
			fabric-particles-v1: Fabric Particles (v1) 5.0.19+d1756aa99e
			fabric-permission-api-v1: Fabric Permission API (v1) 1.0.5+e442d8d09e
			fabric-recipe-api-v1: Fabric Recipe API (v1) 9.0.22+11e1c9a39e
			fabric-registry-sync-v0: Fabric Registry Sync (v0) 7.1.1+c7bd5b8e9e
			fabric-renderer-api-v1: Fabric Renderer API (v1) 14.1.4+2b0d8a229e
			fabric-renderer-indigo: Fabric Renderer - Indigo 9.1.4+2b0d8a229e
			fabric-rendering-fluids-v1: Fabric Rendering Fluids (v1) 6.0.4+06488ac19e
			fabric-rendering-v1: Fabric Rendering (v1) 25.3.3+515ac5339e
			fabric-resource-conditions-api-v1: Fabric Resource Conditions API (v1) 6.1.0+10e9a28b9e
			fabric-resource-loader-v0: Fabric Resource Loader (v0) 3.3.20+4fc5413f9e
			fabric-resource-loader-v1: Fabric Resource Loader (v1) 2.0.13+9edec1269e
			fabric-screen-api-v1: Fabric Screen API (v1) 5.2.1+5087f8249e
			fabric-serialization-api-v1: Fabric Serialization API (v1) 2.0.4+11a26f319e
			fabric-sound-api-v1: Fabric Sound API (v1) 2.0.5+11a26f319e
			fabric-tag-api-v1: Fabric Tag API (v1) 2.1.4+515ac5339e
			fabric-transfer-api-v1: Fabric Transfer API (v1) 8.0.13+11dbb7d79e
			fabric-transitive-access-wideners-v1: Fabric Transitive Access Wideners (v1) 8.1.4+67c847259e
		fabricloader: Fabric Loader 0.20.1
			mixinextras: MixinExtras 0.5.5
		ferritecore: FerriteCore 9.0.0
		freecam: Freecam 1.5.1
		geckolib: GeckoLib 5 5.5.5
		immediatelyfast: ImmediatelyFast 1.16.5+26.2
		iris: Iris 1.11.4+mc26.2
			io_github_douira_glsl-transformer: glsl-transformer 3.0.0-pre3
			org_anarres_jcpp: jcpp 1.4.14
			org_antlr_antlr4-runtime: antlr4-runtime 4.13.1
		java: OpenJDK 64-Bit Server VM 25
		lithium: Lithium 0.25.3+mc26.2
		marlowcrystal: Marlow's Crystal Optimizer 2.0.0
		minecraft: Minecraft 26.2
		moreculling: More Culling 1.8.1
			conditional-mixin: conditional mixin 0.6.3
			mixinsquared: MixinSquared 0.2.0
		nodelay: NoDelay 26.2-1.0.0
		oppaclient: Oppa 1.6.2
		primeauthlib: PrimeAuthLib 1.0.0
		sodium: Sodium 0.9.2+mc26.2
		sodium-extra: Sodium Extra 0.9.5+mc26.2
			me_flashyreese_mods_greenlight-api: greenlight-api 0.1.0+mc26.2
		voicechat: Simple Voice Chat 2.6.22+26.2
			voicechat_api: Simple Voice Chat API 2.6.20
	Launched Version: fabric-loader-0.20.1-26.2
	Launcher name: oppa
	Backend library: LWJGL version 3.4.1-snapshot
	Window size: <not initialized>
	Surface Info: <no surface>
	GFLW Platform: null
	Graphics Device: <none>
	GL debug messages: <no renderer available>
	Is Modded: Definitely; Client brand changed to 'fabric'
	Universe: 404
	Type: Client
	Locale: en_US
	System encoding: UTF-8
	File encoding: UTF-8
	CPU: 16x 12th Gen Intel(R) Core(TM) i7-12650H
