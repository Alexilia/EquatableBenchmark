``` ini

BenchmarkDotNet=v0.12.1, OS=Windows 10.0.18363.815 (1909/November2018Update/19H2)
Intel Core i7-7700HQ CPU 2.80GHz (Kaby Lake), 1 CPU, 8 logical and 4 physical cores
  [Host]        : .NET Framework 4.8 (4.8.4150.0), X64 RyuJIT
  .NET 4.7.2    : .NET Framework 4.8 (4.8.4150.0), X64 RyuJIT
  .NET Core 3.0 : .NET Core 3.0.3 (CoreCLR 4.700.20.6603, CoreFX 4.700.20.6701), X64 RyuJIT


```
|       Method |           Job |       Runtime |      Mean |    Error |    StdDev |    Median |       Gen 0 | Gen 1 | Gen 2 |    Allocated |
|------------- |-------------- |-------------- |----------:|---------:|----------:|----------:|------------:|------:|------:|-------------:|
|  ContainsImp |    .NET 4.7.2 |    .NET 4.7.2 |  68.24 ms | 1.355 ms |  1.391 ms |  67.63 ms |           - |     - |     - |            - |
|  ContainsExp |    .NET 4.7.2 |    .NET 4.7.2 |  64.67 ms | 0.592 ms |  0.525 ms |  64.65 ms |           - |     - |     - |            - |
|  ContainsDef |    .NET 4.7.2 |    .NET 4.7.2 | 191.38 ms | 2.512 ms |  2.227 ms | 191.64 ms | 204000.0000 |     - |     - |  641887392 B |
| ContainsBase |    .NET 4.7.2 |    .NET 4.7.2 | 695.65 ms | 5.545 ms |  4.916 ms | 694.66 ms | 408000.0000 |     - |     - | 1283774784 B |
|  OperatorImp |    .NET 4.7.2 |    .NET 4.7.2 |  97.83 ms | 1.954 ms |  4.490 ms |  95.99 ms |           - |     - |     - |            - |
|  OperatorExp |    .NET 4.7.2 |    .NET 4.7.2 | 379.00 ms | 7.285 ms | 10.903 ms | 376.18 ms | 408000.0000 |     - |     - | 1283774784 B |
|  ContainsImp | .NET Core 3.0 | .NET Core 3.0 |  30.28 ms | 0.601 ms |  0.618 ms |  30.10 ms |           - |     - |     - |            - |
|  ContainsExp | .NET Core 3.0 | .NET Core 3.0 |  42.60 ms | 0.603 ms |  0.534 ms |  42.65 ms |           - |     - |     - |            - |
|  ContainsDef | .NET Core 3.0 | .NET Core 3.0 | 177.17 ms | 3.510 ms |  4.921 ms | 176.67 ms | 204000.0000 |     - |     - |  640000064 B |
| ContainsBase | .NET Core 3.0 | .NET Core 3.0 | 577.74 ms | 8.189 ms |  7.660 ms | 580.39 ms | 408000.0000 |     - |     - | 1280000000 B |
|  OperatorImp | .NET Core 3.0 | .NET Core 3.0 |  92.51 ms | 1.821 ms |  1.789 ms |  92.80 ms |           - |     - |     - |            - |
|  OperatorExp | .NET Core 3.0 | .NET Core 3.0 | 293.49 ms | 5.777 ms |  7.908 ms | 290.47 ms | 204000.0000 |     - |     - |  640000128 B |
