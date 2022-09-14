# cs332-assign
**POSTECH CSED332(Software Design Method) course assignment**
---
## Development Environment
* **OS**: macOS Monterey(MacBook Air M1)
* **JDK**: [Java SE 8](https://www.oracle.com/java/technologies/downloads/#java8)
* **sbt**: 0.13.7(project) / 1.7.1(script version, latest)  

### How to setup environment in macOS 
  
**JDK Setup**
1. Download & install JDK from [this link](https://www.oracle.com/java/technologies/downloads/#java8)
2. Install jEnv
    ```bash
    brew install jenv
    echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.zshrc
    echo 'eval "$(jenv init -)"' >> ~/.zshrc
    ```
3. Find JDK path
    ```bash
    /usr/libexec/java_home -V
    ``` 
4. Add JDK to jEnv
    ```bash
    jenv add {JDK_path}
    # example: jenv add /Library/Java/JavaVirtualMachines/jdk1.8.0_341.jdk/Contents/Home
    ```
5. Configure global JDK version
    ```bash
    # list managed JDKs
    jenv versions

    # configure global version
    jenv global {version} # e.g. jenv global 1.8
    ```
6. Restart terminal 
  
---
**sbt Setup**  
[**Reference**](https://docs.scala-lang.org/getting-started/index.html)
```bash
brew install coursier/formulas/coursier && cs setup
```
---
**Test Setup**
1. Open a project from `build.sbt` with an IDE/VS Code. If you are comfortable using terminal, `cd` into directory which has `build.sbt`.
2. Run `sbt`. This opens up the sbt console.
3. Type `~run`. The `~` is optional and causes sbt to re-run on every file save, allowing for a fast edit/run/debug cycle. sbt will also generate a `target` directory which you can ignore.  

When you’re finished experimenting with this project, press `Enter` to interrupt the run command. Then type `exit` or press `Ctrl+D` to exit sbt and return to your command line prompt.