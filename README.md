# -Virtual-Machines-Linux-Swift-Compiler-Running-the-Swift-Compiler-on-Ubuntu-16.04
To run the Swift compiler on Ubuntu 16.04, you'll need to follow several steps to set up your environment and run Swift code directly on the machine. The following steps guide you through installing Swift on Ubuntu 16.04, running Swift code, and setting up a basic Swift project.
Steps to Install Swift Compiler on Ubuntu 16.04

    Install Dependencies: First, ensure your system is up to date and install the necessary dependencies.

    Open your terminal and run:

sudo apt-get update
sudo apt-get upgrade
sudo apt-get install -y clang libicu-dev libssl-dev libcurl4-openssl-dev

Install Swift: Now, you need to install Swift on your Ubuntu system. The easiest way to install Swift is to use the Swift official repository.

    Download the Swift release for Ubuntu from the official Swift Downloads page. Ensure you choose the Ubuntu 16.04 release.

For instance, download Swift 5.x for Ubuntu 16.04 from this URL:

wget https://swift.org/builds/swift-5.x-release/ubuntu1604/swift-5.x-RELEASE/swift-5.x-RELEASE-ubuntu16.04.tar.gz

Extract the downloaded archive:

tar xzf swift-5.x-RELEASE-ubuntu16.04.tar.gz

Set Up Swift Environment: Move the extracted Swift directory to a proper location, such as /usr/share/swift, and set up the environment variables.

sudo mv swift-5.x-RELEASE-ubuntu16.04 /usr/share/swift

Add Swift to your PATH by adding the following line to your .bashrc or .zshrc (depending on the shell you use).

Open .bashrc:

nano ~/.bashrc

Add this line at the end of the file:

export PATH=/usr/share/swift/usr/bin:$PATH

Then, source the .bashrc file to apply changes:

source ~/.bashrc

Verify Swift Installation: Now that everything is set up, verify that Swift is correctly installed by running:

    swift --version

    This should print the Swift version that you installed. If you see the version output, you're all set.

Running Swift Code on Ubuntu

Once Swift is installed, you can run Swift code either interactively or by writing a Swift script.
Method 1: Interactive Swift Shell

You can use the Swift REPL (Read-Eval-Print Loop) to execute Swift code interactively.

To start the Swift REPL, simply type:

swift

Now you can enter Swift commands interactively. For example:

print("Hello, Swift on Ubuntu!")

Method 2: Running a Swift Script File

Alternatively, you can write Swift code in a .swift file and execute it.

    Create a Swift File:

    Create a file called hello.swift:

nano hello.swift

Add your Swift code to this file. For example:

print("Hello, Swift on Ubuntu!")

Run the Swift File:

To run the Swift file, use the following command:

swift hello.swift

This will execute the Swift code in the hello.swift file, and you'll see the output:

    Hello, Swift on Ubuntu!

Compiling Swift Code into Executable (Optional)

You can also compile Swift code into an executable binary for better performance, rather than running it through the interpreter.

    Create a Swift File (e.g., hello.swift):

print("Hello, Swift on Ubuntu!")

Compile the Swift Code:

To compile the code, use the swiftc command:

swiftc -o hello hello.swift

This will compile the code and generate an executable file named hello.

Run the Compiled Program:

You can now run the compiled program:

./hello

This will print the output:

    Hello, Swift on Ubuntu!

Summary

To summarize, the following steps were involved in running the Swift Compiler on Ubuntu 16.04:

    Installed required dependencies.
    Downloaded and installed the Swift compiler.
    Set up the environment by modifying the PATH variable.
    Ran Swift code interactively via the REPL or as a script.
    Optionally compiled Swift code into a binary using swiftc.

Now you have Swift set up on your Ubuntu 16.04 system, and you can start building and running Swift applications!
