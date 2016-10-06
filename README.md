# Soft-View



## Requirment
 - JDK 7 or higher [link][JDK]
 - JAVA IDE
  - [IntelliJ]
    (for Kasetsart suduent, you can register for education license which will give you all acess to Jetbrain product. Sign Up [HERE][JetvrainStudent])
  - [Eclipse]
 - Expert System Tool
  - [CLIPS-JNI][CLIPS-JNI] [![CLIPS-logo]][CLIPS-JNI]
  
## Get Started
- import CLIPS JNI Library in to the IDE(CLIPSJNI.jar)
- copy CLIPSJNI.dll, CLIPsJNI32.dll, CLIPSJNI64.dll to project directory.
  ```
  +-- out
  +-- src
  |   +-- main.java
  +-- CLIPSJNI.dll
  +-- CLIPSJNI32.dll
  +-- CLIPSJNI64.dll
  ```

- creating CLIPS environment

  ```Java
    Environment clips = new Environment();
  ```
- Inserting knowledge into the knowledge base

  ```Java
    clips.assertString("(colour green)");
  ```
- Evaluating knowledge in the Knowledge base

  ```Java
    System.out.print(clips.eval("(facts)"));
  ```
- output

  ```
    f-0     (initial-fact)
    f-1     (colour green)
    For a total of 2 facts.
  ```
- loading CLIPS file, use for seperating the knowledge base from the software logic.
  
  ```Java
    clips.loadFromResource("bcengine.clp");
  ```
- reset the environemt
  
   ```Java
    Clips.reset();
   ```
-
[JDK]: http://www.oracle.com/technetwork/java/javase/downloads/index.html
[Eclipse]: https://eclipse.org/downloads/
[IntelliJ]: https://www.jetbrains.com/idea/
[JetbrainStudent]: https://www.jetbrains.com/student/
[CLIPS-JNI]:https://sourceforge.net/projects/clipsrules/files/CLIPS/6.30/clips_jni_050.zip/download
[CLIPS-logo]: https://a.fsdn.com/allura/p/clipsrules/icon
