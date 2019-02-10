# c#-optemization-checklist
A checklist for making sure your apps run as efficiently as possible.

# NGen
- On windows, it's most likely located under C:\Windows\Microsoft.NET\Framework64\v4.(ish)\ngen.exe

This tool will precompile many of your dlls to reduce JIT compilation by up to 25x!

# RyuJIT
A c++ inspired compiler which also drastically reduces JIT compilation time by caching many of your app's dlls.

# MPGO
Managed Profile Guided Optimization Tool is useful for precomplilation in combination with NGen. This tool profiles native image assemblies to decrease load time. MPGO also increases memory utilization and throughput by gathering data from training scenarios and using it to optimize the layout of native images.

# StringBuilder
This class can decrease the amount of time it takes to concatenate strings, however it has some serious overhead and should only be used when there is a lot of string concatenation.
