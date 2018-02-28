# FXMLUtils
Class to start controller with FXML layout.

Using Maven, FXML files must stay within the standard **resources** folder.

Also *application.png* must be inside the resources folder (if you want to use an application icon).

Example of use:
```
import javafx.application.Application;
import javafx.scene.control.Alert;
import javafx.stage.Modality;
import javafx.stage.Stage;
import java.io.IOException;

public class Main extends Application {

    @Override
    public void start(Stage primaryStage) {
        try {
            FXMLUtils.openWindow("/main.fxml", "Your window title", 1200, 800, true, Modality.NONE);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```
