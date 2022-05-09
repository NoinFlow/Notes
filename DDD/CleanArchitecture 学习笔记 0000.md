### 动机
```
A: 听说 DDD 很厉害, 想学.
B: 那就学呗.
A: 那么多 DDD 框架学哪个?
B: 你用什么语言?
A: C#
B: 试试 CleanArchitecture
```
### 环境
- Mac OS
- Visual Studio Code
- .Net SDK (6.0.202)

### 行动

- 找到项目
    - [地址](https://github.com/ardalis/CleanArchitecture)

### 引导
- Step 1 安装模板
```
dotnet new --install Ardalis.CleanArchitecture.Template::6.0.10
```
- Step 2 创建模板项目
```
dotnet new clean-arch -o CleanArchitecture
```
- Step 3 进入项目文件夹
```
cd CleanArchitecture
```
- Step 4 补充开发工程依赖
```
cd src
cd CleanArchitecture.Core
dotnet restore
cd ..
cd CleanArchitecture.SharedKernel
dotnet restore
cd ..
cd CleanArchitecture.Infrastructure
dotnet restore
cd ..
cd CleanArchitecture.Web
dotnet restore
cd ../..
```
- Step 5 补充测试工程依赖
```
cd tests
cd CleanArchitecture.UnitTests
dotnet restore
cd ..
cd CleanArchitecture.FunctionalTests
dotnet restore
cd ..
cd CleanArchitecture.IntegrationTests
dotnet restore
cd ../..
```
- Step 6 运行 CleanArchitecture
```
cd src/CleanArchitecture.Web
dotnet run
```