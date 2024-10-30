# kernel-mode-injector
Kernel-mode DLL injector. Nearly undetectable to most anti-cheat solutions.


# About 
* How it works
Kernel-Level Privileges: The injector needs kernel-level privileges, meaning it must run with administrative rights. This is usually done by writing a driver that can interact directly with the operating system's kernel.

Identifying Target Process: The injector must identify the target process into which the DLL will be injected. This typically involves enumerating processes running on the system.

Manipulating Process Memory: The injector will manipulate the memory of the target process. This may involve:

    Allocating memory within the target process's address space.
    Writing the path of the DLL to the allocated memory.

Creating a Remote Thread: To load the DLL, the injector usually creates a remote thread in the target process that calls LoadLibrary. This is done to execute the DLL’s entry point, allowing it to run within the context of the target process.

Hiding from Detection: To remain undetected, injectors often employ techniques such as:

    Code Obfuscation: Making the injector code difficult to read or analyze.
    Avoiding Common Detection Patterns: Such as avoiding known API calls that anti-cheat solutions monitor.

* How to use
Run the executable as admin, select your desired DLL, select your desired process (via process id) and inject.
This injector makes it invisible to programs like process hacker where you can view a programs current DLLs.

* Anti-Cheats
This injector is currently only detected by VGK/Vanguard, but we hope to bypass them in the future.

* THIS PROJECT WILL BE CLOSED SOURCE FOR MULTIPLE REASONS
1 - Will be detected faster
2 - AC's will take the project, see how it works and block the methods used
3 - Methods used are considered extremely private
