
---- Minecraft Crash Report ----
// Surprise! Haha. Well, this is awkward.

Time: 18.2.22 17:53
Description: mouseClicked event handler

java.lang.IllegalArgumentException: Name and ID cannot both be blank
	at com.mojang.authlib.GameProfile.<init>(GameProfile.java:26) ~[authlib-2.1.28.jar:?] {re:computing_frames,re:classloading}
	at com.mojang.authlib.yggdrasil.YggdrasilMinecraftSessionService.fillGameProfile(YggdrasilMinecraftSessionService.java:192) ~[authlib-2.1.28.jar:?] {re:classloading,re:classloading,re:classloading,re:classloading}
	at com.mojang.authlib.yggdrasil.YggdrasilMinecraftSessionService.fillProfileProperties(YggdrasilMinecraftSessionService.java:179) ~[authlib-2.1.28.jar:?] {re:classloading,re:classloading,re:classloading,re:classloading}
	at net.minecraft.client.Minecraft.loadWorld(Minecraft.java:1799) ~[?:?] {re:classloading,pl:accesstransformer:B,pl:runtimedistcleaner:A}
	at net.minecraft.client.Minecraft.func_238192_a_(Minecraft.java:1687) ~[?:?] {re:classloading,pl:accesstransformer:B,pl:runtimedistcleaner:A}
	at net.minecraft.client.gui.screen.CreateWorldScreen.func_195352_j(CreateWorldScreen.java:260) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.gui.screen.CreateWorldScreen.lambda$init$11(CreateWorldScreen.java:205) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.gui.widget.button.Button.func_230930_b_(SourceFile:33) ~[?:?] {re:classloading}
	at net.minecraft.client.gui.widget.button.AbstractButton.func_230982_a_(SourceFile:16) ~[?:?] {re:classloading}
	at net.minecraft.client.gui.widget.Widget.func_231044_a_(Widget.java:136) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.gui.INestedGuiEventHandler.func_231044_a_(SourceFile:27) ~[?:?] {re:classloading}
	at net.minecraft.client.MouseHelper.func_198033_b(MouseHelper.java:87) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.gui.screen.Screen.func_231153_a_(Screen.java:427) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.MouseHelper.func_198023_a(MouseHelper.java:85) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.MouseHelper.func_228030_c_(MouseHelper.java:181) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.util.concurrent.ThreadTaskExecutor.execute(ThreadTaskExecutor.java:111) ~[?:?] {re:classloading,pl:accesstransformer:B,xf:OptiFine:default}
	at net.minecraft.client.MouseHelper.func_228028_b_(MouseHelper.java:180) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at org.lwjgl.glfw.GLFWMouseButtonCallback$Container.invoke(GLFWMouseButtonCallback.java:81) ~[lwjgl-glfw-classes.jar:?] {}
	at org.lwjgl.glfw.GLFW.glfwPollEvents(GLFW.java:1161) ~[lwjgl-glfw-classes.jar:?] {}
	at com.mojang.blaze3d.systems.RenderSystem.flipFrame(SourceFile:102) ~[?:?] {re:classloading}
	at net.minecraft.client.MainWindow.func_227802_e_(MainWindow.java:398) ~[?:?] {re:classloading,xf:OptiFine:default}
	at net.minecraft.client.Minecraft.func_195542_b(Minecraft.java:997) ~[?:?] {re:classloading,pl:accesstransformer:B,pl:runtimedistcleaner:A}
	at net.minecraft.client.Minecraft.func_99999_d(Minecraft.java:607) ~[?:?] {re:classloading,pl:accesstransformer:B,pl:runtimedistcleaner:A}
	at net.minecraft.client.main.Main.main(Main.java:184) ~[1.16.5-forge-36.2.20.jar:?] {re:classloading,pl:runtimedistcleaner:A}
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0-internal] {}
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0-internal] {}
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0-internal] {}
	at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0-internal] {}
	at net.minecraftforge.fml.loading.FMLClientLaunchProvider.lambda$launchService$0(FMLClientLaunchProvider.java:51) ~[forge-1.16.5-36.2.20.jar:36.2] {}
	at cpw.mods.modlauncher.LaunchServiceHandlerDecorator.launch(LaunchServiceHandlerDecorator.java:37) [modlauncher-8.0.9.jar:?] {}
	at cpw.mods.modlauncher.LaunchServiceHandler.launch(LaunchServiceHandler.java:54) [modlauncher-8.0.9.jar:?] {}
	at cpw.mods.modlauncher.LaunchServiceHandler.launch(LaunchServiceHandler.java:72) [modlauncher-8.0.9.jar:?] {}
	at cpw.mods.modlauncher.Launcher.run(Launcher.java:82) [modlauncher-8.0.9.jar:?] {}
	at cpw.mods.modlauncher.Launcher.main(Launcher.java:66) [modlauncher-8.0.9.jar:?] {}


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Render thread
Stacktrace:
	at com.mojang.authlib.GameProfile.<init>(GameProfile.java:26) ~[authlib-2.1.28.jar:?] {re:computing_frames,re:classloading}
	at com.mojang.authlib.yggdrasil.YggdrasilMinecraftSessionService.fillGameProfile(YggdrasilMinecraftSessionService.java:192) ~[authlib-2.1.28.jar:?] {re:classloading,re:classloading,re:classloading,re:classloading,re:classloading}
	at com.mojang.authlib.yggdrasil.YggdrasilMinecraftSessionService.fillProfileProperties(YggdrasilMinecraftSessionService.java:179) ~[authlib-2.1.28.jar:?] {re:classloading,re:classloading,re:classloading,re:classloading,re:classloading}
	at net.minecraft.client.Minecraft.loadWorld(Minecraft.java:1799) ~[?:?] {re:classloading,pl:accesstransformer:B,pl:runtimedistcleaner:A}
	at net.minecraft.client.Minecraft.func_238192_a_(Minecraft.java:1687) ~[?:?] {re:classloading,pl:accesstransformer:B,pl:runtimedistcleaner:A}
	at net.minecraft.client.gui.screen.CreateWorldScreen.func_195352_j(CreateWorldScreen.java:260) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.gui.screen.CreateWorldScreen.lambda$init$11(CreateWorldScreen.java:205) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.gui.widget.button.Button.func_230930_b_(SourceFile:33) ~[?:?] {re:classloading}
	at net.minecraft.client.gui.widget.button.AbstractButton.func_230982_a_(SourceFile:16) ~[?:?] {re:classloading}
	at net.minecraft.client.gui.widget.Widget.func_231044_a_(Widget.java:136) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.gui.INestedGuiEventHandler.func_231044_a_(SourceFile:27) ~[?:?] {re:classloading}
	at net.minecraft.client.MouseHelper.func_198033_b(MouseHelper.java:87) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
-- Affected screen --
Details:
	Screen name: net.minecraft.client.gui.screen.CreateWorldScreen
Stacktrace:
	at net.minecraft.client.gui.screen.Screen.func_231153_a_(Screen.java:427) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.MouseHelper.func_198023_a(MouseHelper.java:85) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.client.MouseHelper.func_228030_c_(MouseHelper.java:181) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at net.minecraft.util.concurrent.ThreadTaskExecutor.execute(ThreadTaskExecutor.java:111) ~[?:?] {re:classloading,pl:accesstransformer:B,xf:OptiFine:default}
	at net.minecraft.client.MouseHelper.func_228028_b_(MouseHelper.java:180) ~[?:?] {re:classloading,pl:runtimedistcleaner:A}
	at org.lwjgl.glfw.GLFWMouseButtonCallback$Container.invoke(GLFWMouseButtonCallback.java:81) ~[lwjgl-glfw-classes.jar:?] {}
	at org.lwjgl.glfw.GLFW.glfwPollEvents(GLFW.java:1161) ~[lwjgl-glfw-classes.jar:?] {}
	at com.mojang.blaze3d.systems.RenderSystem.flipFrame(SourceFile:102) ~[?:?] {re:classloading}
	at net.minecraft.client.MainWindow.func_227802_e_(MainWindow.java:398) ~[?:?] {re:classloading,xf:OptiFine:default}
	at net.minecraft.client.Minecraft.func_195542_b(Minecraft.java:997) ~[?:?] {re:classloading,pl:accesstransformer:B,pl:runtimedistcleaner:A}
	at net.minecraft.client.Minecraft.func_99999_d(Minecraft.java:607) ~[?:?] {re:classloading,pl:accesstransformer:B,pl:runtimedistcleaner:A}
	at net.minecraft.client.main.Main.main(Main.java:184) ~[1.16.5-forge-36.2.20.jar:?] {re:classloading,pl:runtimedistcleaner:A}
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0-internal] {}
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0-internal] {}
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0-internal] {}
	at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0-internal] {}
	at net.minecraftforge.fml.loading.FMLClientLaunchProvider.lambda$launchService$0(FMLClientLaunchProvider.java:51) ~[forge-1.16.5-36.2.20.jar:36.2] {}
	at cpw.mods.modlauncher.LaunchServiceHandlerDecorator.launch(LaunchServiceHandlerDecorator.java:37) [modlauncher-8.0.9.jar:?] {}
	at cpw.mods.modlauncher.LaunchServiceHandler.launch(LaunchServiceHandler.java:54) [modlauncher-8.0.9.jar:?] {}
	at cpw.mods.modlauncher.LaunchServiceHandler.launch(LaunchServiceHandler.java:72) [modlauncher-8.0.9.jar:?] {}
	at cpw.mods.modlauncher.Launcher.run(Launcher.java:82) [modlauncher-8.0.9.jar:?] {}
	at cpw.mods.modlauncher.Launcher.main(Launcher.java:66) [modlauncher-8.0.9.jar:?] {}


-- System Details --
Details:
	Minecraft Version: 1.16.5
	Minecraft Version ID: 1.16.5
	Operating System: Linux (aarch64) version Android-11
	Java Version: 1.8.0-internal, Oracle Corporation
	Java VM Version: OpenJDK 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 2538965744 bytes (2421 MB) / 3036676096 bytes (2896 MB) up to 3036676096 bytes (2896 MB)
	CPUs: 6
	JVM Flags: 8 total; -XX:+UnlockExperimentalVMOptions -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M -Xms3052M -Xmx3052M -Xbootclasspath/p:/storage/emulated/0/Android/data/net.kdt.pojavlaunch/files/caciocavallo/ResConfHack.jar:/storage/emulated/0/Android/data/net.kdt.pojavlaunch/files/caciocavallo/cacio-androidnw-1.10-SNAPSHOT.jar:/storage/emulated/0/Android/data/net.kdt.pojavlaunch/files/caciocavallo/cacio-shared-1.10-SNAPSHOT.jar
	ModLauncher: 8.0.9+86+master.3cf110c
	ModLauncher launch target: fmlclient
	ModLauncher naming: srg
	ModLauncher services: 
		/mixin-0.8.4.jar mixin PLUGINSERVICE 
		/eventbus-4.0.0.jar eventbus PLUGINSERVICE 
		/forge-1.16.5-36.2.20.jar object_holder_definalize PLUGINSERVICE 
		/forge-1.16.5-36.2.20.jar runtime_enum_extender PLUGINSERVICE 
		/accesstransformers-3.0.1.jar accesstransformer PLUGINSERVICE 
		/forge-1.16.5-36.2.20.jar capability_inject_definalize PLUGINSERVICE 
		/forge-1.16.5-36.2.20.jar runtimedistcleaner PLUGINSERVICE 
		/mixin-0.8.4.jar mixin TRANSFORMATIONSERVICE 
		/OptiFine_1.16.5_HD_U_G8.jar OptiFine TRANSFORMATIONSERVICE 
		/forge-1.16.5-36.2.20.jar fml TRANSFORMATIONSERVICE 
	FML: 36.2
	Forge: net.minecraftforge:36.2.20
	FML Language Providers: 
		javafml@36.2
		minecraft@1
	Mod List: 
		forge-1.16.5-36.2.20-client.jar                   |Minecraft                     |minecraft                     |1.16.5              |DONE      |Manifest: NOSIGNATURE
		AmbientSounds_v3.1.11_mc1.16.5.jar                |Ambient Sounds                |ambientsounds                 |3.0.3               |DONE      |Manifest: NOSIGNATURE
		forge-1.16.5-36.2.20-universal.jar                |Forge                         |forge                         |36.2.20             |DONE      |Manifest: 22:af:21:d8:19:82:7f:93:94:fe:2b:ac:b7:e4:41:57:68:39:87:b1:a7:5c:c6:44:f9:25:74:21:14:f5:0d:90
		DynamicSurroundings-1.16.5-4.0.5.0.jar            |ยง3Dynamic Surroundings        |dsurround                     |4.0.5.0             |DONE      |Manifest: NOSIGNATURE
		CreativeCore_v2.2.1_mc1.16.5.jar                  |CreativeCore                  |creativecore                  |2.0.0               |DONE      |Manifest: NOSIGNATURE
	Crash Report UUID: 8c0c5c10-c4a6-4f77-b504-48374db5f3e2
	Launched Version: 1.16.5
	Backend library: LWJGL version 3.2.3 SNAPSHOT
	Backend API: GL4ES wrapper GL version 2.1 gl4es wrapper 1.1.4, ptitSeb
	GL Caps: Using framebuffer using ARB_framebuffer_object extension
	Using VBOs: Yes
	Is Modded: Definitely; Client brand changed to 'forge'
	Type: Client (map_client.txt)
	GPU Warnings: version: 2.1
	Graphics mode: fancy
	Resource Packs: vanilla, mod_resources
	Current Language: English (US)
	CPU: 9x null
	OptiFine Version: OptiFine_1.16.5_HD_U_G8
	OptiFine Build: 20210515-161946
	Render Distance Chunks: 2
	Mipmaps: 0
	Anisotropic Filtering: 1
	Antialiasing: 0
	Multitexture: false
	Shaders: null
	OpenGlVersion: 2.1 gl4es wrapper 1.1.4
	OpenGlRenderer: GL4ES wrapper
	OpenGlVendor: ptitSeb
	CpuCount: 6
