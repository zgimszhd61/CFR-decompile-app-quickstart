# java-decompile-app-quickstart（从jar包得到源代码的技术）
## 安装
反编译JAR文件可以帮助我们查看编译后的Java字节码并将其转换回可读的Java源代码。以下是几种常用的反编译工具和方法，以及一个具体的例子来演示如何反编译JAR文件。

## 常用的Java反编译工具

1. **JD-GUI**：一个图形化的Java反编译工具，支持Windows、Mac和Linux平台[2][12]。
2. **Procyon**：一个开源的Java反编译器，能够处理复杂的Java代码[4][13]。
3. **CFR**：一个支持现代Java特性的反编译器，能够处理Java 8及以上版本的代码[3][13]。
4. **FernFlower**：IntelliJ IDEA内置的反编译器，也可以作为独立工具使用[8][13]。

## 具体的反编译例子

### 使用JD-GUI反编译JAR文件

1. **下载并安装JD-GUI**：
   - 从[JD-GUI官网](http://jd.benow.ca/)下载JD-GUI。
   - 解压并运行JD-GUI。

2. **打开JAR文件**：
   - 在JD-GUI中，点击“File”菜单，然后选择“Open File...”，导航到你想要反编译的JAR文件并打开它。
   - JD-GUI会自动开始反编译，并在主窗口中显示反编译后的源代码。

3. **保存反编译后的源代码**：
   - 在JD-GUI中，点击“File”菜单，然后选择“Save All Sources...”，选择一个目录来保存反编译后的Java源文件。

### 使用Procyon反编译JAR文件

1. **下载Procyon反编译器**：
   - 从[Procyon官网](https://bitbucket.org/mstrobel/procyon/wiki/Java%20Decompiler)下载Procyon反编译器。

2. **运行反编译命令**：
   - 打开命令行终端，导航到Procyon反编译器所在的目录。
   - 使用以下命令反编译JAR文件：
     ```bash
     java -jar procyon-decompiler.jar example.jar
     ```
   - 这将提取JAR文件中的所有类文件，并将反编译后的源代码保存为与类文件同名的.java文件。

### 使用CFR反编译JAR文件 【已试用】

1. **下载CFR反编译器**： 
   - 从[CFR官网](http://www.benf.org/other/cfr/)下载CFR反编译器。

2. **运行反编译命令**：
   - 打开命令行终端，导航到CFR反编译器所在的目录。
   - 使用以下命令反编译JAR文件：
     ```bash
     java -jar cfr.jar example.jar --outputdir ./decompiled
     ```
   - 这将把反编译后的源代码保存到指定的输出目录中。

### 使用FernFlower反编译JAR文件 【更新频繁】

1. **下载FernFlower反编译器**：
   - 从[FernFlower GitHub仓库](https://github.com/fesh0r/fernflower)克隆源代码并构建反编译器。

2. **运行反编译命令**：
   - 打开命令行终端，导航到FernFlower反编译器所在的目录。
   - 使用以下命令反编译JAR文件：
     ```bash
     java -jar fernflower.jar example.jar ./decompiled
     ```
   - 这将把反编译后的源代码保存到指定的输出目录中。

## 注意事项

- 反编译的代码可能不完全准确，可能会有错误或不完整的地方。
- 反编译代码的合法性取决于具体情况，通常反编译第三方库可能会违反版权规定，因此应谨慎使用。

通过以上步骤，你可以使用不同的工具来反编译JAR文件并查看其源代码。选择适合你的工具和方法，确保遵守相关法律法规。



## 使用
 - 第一步： 从https://mvnrepository.com/ 进去看项目。
 - 第二步： 到maven仓库去下载对应的mvn包，譬如：https://repo1.maven.org/maven2/com/google/code/gson/gson/2.8.8/
<img width="664" alt="image" src="https://github.com/zgimszhd61/CFR-decompile-app-quickstart/assets/114722053/33aa9d92-0543-49c1-a4a7-18078d5acb0d">
 - 记得下载不带sources和javadoc后缀的。
