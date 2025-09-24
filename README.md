# Vityarthi-java-project
Campus Course & Records Manager (CCRM)

Project Overview The Campus Course & Records Manager (CCRM) is a console-based Java application designed to manage student records, courses, and enrollments for an educational institution. It demonstrates core Java SE principles, including a layered architecture, object-oriented design, and modern Java APIs like Streams and NIO.2 for file handling.

Evolution of Java (Short Timeline)
In 1991, James Gosling started the Green Project at Sun Microsystems, which became Java.

Java 1.0 was officially released in 1995 with the promise “Write Once, Run Anywhere.”

In 1997, JDK 1.1 was released and the Java Community Process (JCP) was established.

Java 2 (J2SE 1.2) came out in 1998 introducing Swing and the Collections framework.

In 2006, Sun renamed J2SE, J2EE, and J2ME to Java SE, Java EE, and Java ME.

Oracle acquired Sun Microsystems in 2009, taking stewardship of Java.

Java 8 was released in 2014, adding Lambda expressions and Streams API.

Java 9 introduced the module system in 2017.

Java 17 launched as a long-term support release in 2021.

Java continues evolving with new features and performance improvements.

Difference between Java ME, Java SE, and Java EE
Java ME (Micro Edition) is a lightweight version of Java designed for small devices like mobile phones and embedded systems. It provides limited APIs optimized for constrained resources.

Java SE (Standard Edition) is the core Java platform for desktop and server applications. It includes the basic APIs for general-purpose programming including GUI, networking, and utilities.

Java EE (Enterprise Edition) builds on Java SE and adds specialized APIs and tools for large-scale, distributed, multi-tier enterprise applications including web services, messaging, transaction management, and persistence.

Java Architecture: JDK, JRE, JVM
JVM (Java Virtual Machine) is the component that interprets compiled Java bytecode and executes it as machine code. It is platform-dependent.

JRE (Java Runtime Environment) includes the JVM plus the standard Java class libraries and runtime environment needed to run Java applications.

JDK (Java Development Kit) contains the JRE along with development tools such as compiler (javac), debugger, and other utilities. It is used to develop Java programs.

JDK compiles source code to bytecode. JRE provides the libraries and environment to run the bytecode. JVM runs the bytecode on the specific platform.

How to Install & Configure Java on Windows
Download the JDK installer from the Oracle website.

Run the installer and follow the installation wizard.

Set the environment variable JAVA_HOME to the installation path of JDK.

Add %JAVA_HOME%\bin to the system PATH variable so Java commands can be run from anywhere.

Verify installation by opening Command Prompt and running java -version and javac -version.

Using Eclipse IDE: Creating a New Project & Running
To create a new project:

Open Eclipse.

Go to File > New > Java Project.

Enter project name and click Finish.

Right-click on src folder and select New > Class to create a new Java class.

To run the project or a file:

Right-click on the Java file.

Select Run As > Java Application.

For more options, go to Run > Run Configurations to set arguments or environment variables, then run.

2025: Java continues to evolve with new features and performance improvements.
Mapping: Syllabus Topic → Project Implementation

[cite_start]This table maps the mandatory technical requirements to their implementation locations within the project's source code, as required[cite: 136].

| Syllabus Topic/Requirement | Location in Project (src/ folder) |
| :--- | :--- |
| *OOP: Encapsulation* | [cite_start]edu.ccrm.domain.Student and Course classes use private fields with public getters/setters[cite: 59]. |
| *OOP: Inheritance & Abstraction* | [cite_start]edu.ccrm.domain.Person is an abstract class [cite: 61] [cite_start]extended by Student and Instructor[cite: 60]. |
| *OOP: Polymorphism* | [cite_start]The TranscriptService uses a Person reference to invoke overridden toString() methods on Student and Instructor objects[cite: 62]. |
| *Interfaces* | [cite_start]edu.ccrm.io.Persistable is an interface implemented by services that handle data import/export[cite: 69]. |
| *Enums with Constructors* | [cite_start]edu.ccrm.domain.Semester and edu.ccrm.domain.Grade are enums with custom fields and constructors[cite: 74, 27]. |
| *Lambdas & Functional Interfaces* | [cite_start]The CourseService class uses lambda expressions with the Stream API for filtering courses by instructor or department[cite: 72, 23]. |
| *Design Pattern: Singleton* | [cite_start]edu.ccrm.config.AppConfig is implemented as a Singleton to manage global application settings[cite: 80]. |
| *Design Pattern: Builder* | [cite_start]The Course class has a static nested CourseBuilder class for object construction[cite: 81]. |
| *Custom Exceptions* | [cite_start]edu.ccrm.util.exceptions.DuplicateEnrollmentException and MaxCreditLimitExceededException are custom checked exceptions[cite: 86, 87, 88]. |
| *File I/O (NIO.2)* | [cite_start]edu.ccrm.io.BackupService uses Path and Files for creating timestamped backup folders and copying files[cite: 91, 32]. |
| *I/O with Streams* | [cite_start]The ImportExportService uses Files.lines() (a Stream) to read and process lines from CSV files[cite: 92]. |
| *Recursion* | [cite_start]edu.ccrm.util.FileUtils contains a recursive method to calculate the total size of a backup directory[cite: 33]. |
| *Date/Time API* | [cite_start]The Student class uses LocalDate for date fields [cite: 18][cite_start], and backups use LocalDateTime for timestamps[cite: 94]. |
| *Nested Classes* | [cite_start]A static nested CourseBuilder is in Course; an inner class is used for a custom comparator in StudentService[cite: 67]. |
| *Assertions* | [cite_start]Assertions are used in service classes to check for invariants like non-null IDs or valid credit values[cite: 89]. |

Main program:
<img width="1593" height="824" alt="Screenshot 2025-09-25 002717" src="https://github.com/user-attachments/assets/7c495586-8640-41cf-b528-6c051390a2dd" />
Output:
<img width="568" height="242" alt="image" src="https://github.com/user-attachments/assets/276f8098-ee5a-44df-a527-5f75d0b1d586" />




