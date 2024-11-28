### What is Maven?
- Maven is a project management and build automation tool used primarily for Java projects.
- It simplifies the build process and manages dependencies (external libraries your project needs).
- It follows a standard project structure, making it easy to manage and maintain projects.
- Uses an XML file (`pom.xml`) to handle project configurations.
- Automates compiling, testing, and packaging your project into formats like `.jar` or `.war`.

### Maven Features  
- **Simple project setup**: Uses a standard directory structure and dependency management, saving time on configuration.
- **Dependency management**: Automatically downloads the right versions of libraries for your project.
- **Build automation**: Compiles, tests, and packages the project without manual steps.
- **Extensibility**: Supports plugins that add features for custom tasks.
- **Multi-module support**: Can manage multiple projects within a larger project.
- **Central repository**: Access to thousands of libraries stored in Maven Central for easy integration.

### Maven vs Ant

| **Feature**           | **Maven**                               | **Ant**                                  |
| --------------------- | --------------------------------------- | ---------------------------------------- |
| **Purpose**           | Project management & build automation   | Task-based build tool                    |
| **Dependency**        | Automatic dependency management         | Requires manual configuration            |
| **Project Structure** | Uses a standard structure (convention)  | No default structure; fully configurable |
| **Configuration**     | Uses `pom.xml` for project info         | Uses custom XML scripts                  |
| **Build Phases**      | Defined phases (compile, test, package) | Manually written tasks                   |

### Maven Installation
1. **Download Maven**: Go to the Apache Maven website and download the binary zip or tar.gz file.
2. **Extract Files**: Unzip or extract the downloaded file to a folder on your system.
3. **Set Environment Variables**:
   - Add `MAVEN_HOME` as a system variable (point it to your Maven folder).
   - Update your `PATH` variable to include Maven’s `bin` directory.
4. **Verify Installation**: Open a terminal/command prompt and run `mvn -version` to confirm Maven is installed correctly.

### Maven Repositories
- **Local Repository**: A folder on your system where Maven stores downloaded dependencies.
- **Central Repository**: A remote, global repository provided by Maven where libraries are fetched automatically.
- **Remote Repository**: Other repositories that can be specified in the `pom.xml` to fetch dependencies not available in the Central Repository.
Maven automatically checks the local repository first, and if a dependency isn't found, it will search in remote/central repositories.

### Maven POM
1. POM stands for Project Model Object.
2. The `pom.xml` file is the core configuration file for a Maven project.
3. It contains details like the project's name, version, and dependencies.
4. It defines plugins, goals, repositories, and project-specific settings.
5. **POM Hierarchy**:
  - **Super POM**: The default POM used by Maven, inherited by all projects.
  - **Parent POM**: You can specify a parent project POM to inherit settings.
  - **Child POM**: Projects that inherit settings from a parent POM.