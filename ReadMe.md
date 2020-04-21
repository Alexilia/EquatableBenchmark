``` ini

BenchmarkDotNet=v0.12.1, OS=Windows 10.0.17763.379 (1809/October2018Update/Redstone5)
Intel Core i7-6700HQ CPU 2.60GHz (Skylake), 1 CPU, 8 logical and 4 physical cores
  [Host]     : .NET Framework 4.7.2 (4.7.3324.0), X86 LegacyJIT
  DefaultJob : .NET Framework 4.7.2 (4.7.3324.0), X86 LegacyJIT


```
|       Method |        Mean |     Error |    StdDev |      Median |       Gen 0 | Gen 1 | Gen 2 |   Allocated |
|------------- |------------:|----------:|----------:|------------:|------------:|------:|------:|------------:|
|  ContainsImp |    80.69 ms |  1.471 ms |  1.807 ms |    80.30 ms |           - |     - |     - |           - |
|  ContainsExp |    86.21 ms |  1.721 ms |  3.275 ms |    85.72 ms |           - |     - |     - |           - |
|  ContainsDef |   271.21 ms |  5.369 ms | 10.216 ms |   268.36 ms | 152500.0000 |     - |     - | 480003442 B |
| ContainsBase | 1,097.65 ms | 21.878 ms | 46.148 ms | 1,082.68 ms | 305000.0000 |     - |     - | 960006884 B |
|  OperatorImp |    91.66 ms |  1.819 ms |  4.253 ms |    90.47 ms |           - |     - |     - |           - |
|  OperatorExp |   647.23 ms | 12.837 ms | 34.042 ms |   636.65 ms | 305000.0000 |     - |     - | 960006884 B |
