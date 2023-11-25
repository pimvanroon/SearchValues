```

BenchmarkDotNet v0.13.10, Windows 10 (10.0.19045.3693/22H2/2022Update)
AMD Ryzen 7 3700X, 1 CPU, 16 logical and 8 physical cores
.NET SDK 8.0.100
  [Host]     : .NET 8.0.0 (8.0.23.53103), X64 RyuJIT AVX2 [AttachedDebugger]
  DefaultJob : .NET 8.0.0 (8.0.23.53103), X64 RyuJIT AVX2


```
| Method                | ExampleText          | Mean       | Error     | StdDev    | Allocated |
|---------------------- |--------------------- |-----------:|----------:|----------:|----------:|
| **IsBase64_SearchValues** | **6iFbuI^pe68k**         |   **3.008 ns** | **0.0118 ns** | **0.0110 ns** |         **-** |
| IsBase64_CharArray    | 6iFbuI^pe68k         |  21.527 ns | 0.1434 ns | 0.1271 ns |         - |
| IsBase64_Naive        | 6iFbuI^pe68k         |  46.077 ns | 0.0920 ns | 0.0861 ns |         - |
| **IsBase64_SearchValues** | **dQw4w9WgXcQ**          |   **2.541 ns** | **0.0129 ns** | **0.0108 ns** |         **-** |
| IsBase64_CharArray    | dQw4w9WgXcQ          |  36.008 ns | 0.1272 ns | 0.1190 ns |         - |
| IsBase64_Naive        | dQw4w9WgXcQ          |  70.583 ns | 0.1789 ns | 0.1586 ns |         - |
| **IsBase64_SearchValues** | **dQw4w(...)WgXcQ [55]** |   **3.759 ns** | **0.0266 ns** | **0.0236 ns** |         **-** |
| IsBase64_CharArray    | dQw4w(...)WgXcQ [55] |  56.252 ns | 0.0727 ns | 0.0680 ns |         - |
| IsBase64_Naive        | dQw4w(...)WgXcQ [55] | 358.390 ns | 0.3718 ns | 0.3296 ns |         - |
