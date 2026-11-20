# JavaFX

These independent desktop lessons cover event handlers, layouts, controls, bindings, CSS and FXML. Use JDK 21 or newer and a compatible JavaFX SDK for your OS (validated with JavaFX 21.0.2). Set `JAVAFX_HOME` to the SDK folder containing `lib`. From the repository root in PowerShell:

```powershell
cd 031_fxml
$fx = "$env:JAVAFX_HOME\lib"
javac --module-path $fx --add-modules javafx.controls,javafx.fxml -d out *.java
Copy-Item sample.fxml out\sample\
java --module-path $fx --add-modules javafx.controls,javafx.fxml -cp out sample.Main
```

Expect a window with a label and a Submit button, and `View is now loaded!` in the console. FXML must be next to `sample.Main` on the classpath. For the other lessons, compile one folder at a time with the same `javac` command and run `Main` rather than `sample.Main`; in `027_css`, copy `Viper.css` to `out\` before launch. A graphical desktop is needed for interactive use. Both lesson resources are included; no JavaFX runtime binaries are bundled.

Validation: All 22 lessons compiled. The simple window, CSS, and FXML scenes launched headlessly; interactive controls were not tested.
