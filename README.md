# Java Journey, 15: Basic Components Of Java Swing.

Repository # 15 covers the basic components of Java Swing, a powerful GUI toolkit for Java applications. The Swing library provides a set of customizable components such as buttons, text fields, labels, panels, and more that can be easily integrated into Java applications. This repository will cover the different types of components available in Java Swing and how to create and customize them to build robust and user-friendly graphical user interfaces.

## JFrame

JFrame is a class in the Java Swing framework that provides a container for creating a top-level window in a Java application. It represents the main window of a GUI application and can be customized with various Swing components to create a user-friendly interface.

Here's an example of creating a JFrame:

```bash
import javax.swing.JFrame;

public class MyFrame extends JFrame {
    public MyFrame() {
        setTitle("My JFrame Example");
        setSize(400, 300);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setVisible(true);
    }
    
    public static void main(String[] args) {
        MyFrame frame = new MyFrame();
    }
}
```

In the above example, we create a subclass of JFrame called MyFrame. We set the title and size of the JFrame using the setTitle and setSize methods, respectively. The setDefaultCloseOperation method specifies that the application should exit when the JFrame is closed. Finally, we make the JFrame visible using the setVisible method. The main method creates an instance of MyFrame, which displays the JFrame on the screen.

We can also add other Swing components to the JFrame, such as buttons, text fields, and labels, to create a more interactive GUI application.

## JPanel

In Java Swing, a JPanel is a container that can hold and organize other components such as buttons, labels, text fields, etc. It is a lightweight component that provides a space to group related components and separate them from other components in the container.

JPanel provides a variety of methods to customize its appearance and behavior, including setting the background color, layout manager, border, and preferred size.

Here's an example of how to create and add components to a JPanel:

```bash
import javax.swing.*;
import java.awt.*;

public class MyPanel extends JPanel {
    public MyPanel() {
        // Set background color
        setBackground(Color.WHITE);

        // Set layout manager
        setLayout(new GridLayout(2, 2));

        // Create components and add them to the panel
        JLabel label = new JLabel("Enter your name:");
        add(label);
        JTextField textField = new JTextField();
        add(textField);
        JButton button = new JButton("Submit");
        add(button);
        JCheckBox checkBox = new JCheckBox("Remember me");
        add(checkBox);
    }
}
```

In this example, we extend the JPanel class to create a custom panel called MyPanel. We set the background color to white and use a GridLayout with two rows and two columns to organize the components. Then, we create a JLabel, JTextField, JButton, and JCheckBox, and add them to the panel using the add() method.

## JButton

JButton is a class in Java Swing that provides a button component for creating interactive buttons in GUI applications. It is a simple way to enable user interaction and trigger events.

The following is an example of how to create a JButton and add it to a JFrame:

```bash
import javax.swing.*;

public class MyFrame extends JFrame {
    public static void main(String[] args) {
        JFrame frame = new JFrame("My Frame");
        frame.setSize(400, 400);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        
        // Create a JButton
        JButton button = new JButton("Click me!");
        
        // Add the JButton to the JFrame
        frame.add(button);
        
        frame.setVisible(true);
    }
}
```

In this example, a JButton is created with the text "Click me!" and added to the JFrame. When the button is clicked, an event can be triggered to perform some action, such as opening a new window or updating data.

## JLabel

JLabel is a Swing component used to display text, images, or both. It is a non-editable text field and is used for descriptive purposes in user interfaces.

To create a JLabel, we can use the following syntax:

```bash
JLabel label = new JLabel();
```

We can also set text and/or an icon for the label by passing them as arguments to the constructor or by calling the setText() and setIcon() methods. For example:

```bash
JLabel label = new JLabel("Hello World!");  // create a label with text
JLabel label2 = new JLabel();               // create an empty label
label2.setText("Click the button.");        // set text for the label

// create an image icon and set it for the label
ImageIcon icon = new ImageIcon("image.jpg");
JLabel label3 = new JLabel(icon);
```

We can also customize the appearance of the label using methods such as setFont(), setForeground(), and setBackground(). For example:

```bash
label.setFont(new Font("Arial", Font.BOLD, 16));    // set font to Arial, bold, size 16
label.setForeground(Color.RED);                    // set text color to red
label.setBackground(Color.YELLOW);                 // set background color to yellow
```

Overall, JLabel is a useful component for displaying text and images in a Java Swing user interface.

## JTextfield

JTextField is a Swing component in Java that provides an editable area for the user to enter and edit text. It extends the JTextComponent class and provides basic text editing functionalities such as copy, paste, undo, and redo.

To create a JTextField object, you can use the following syntax:

```bash
JTextField textField = new JTextField();
```

You can also specify the initial text content and size of the text field like this:

```bash
JTextField textField = new JTextField("Initial Text", 20);
```

This creates a text field with the initial text "Initial Text" and a preferred width of 20 characters.

To get the text entered by the user, you can use the getText() method:

```bash
String text = textField.getText();
```

You can also set the text of the text field programmatically using the setText() method:

```bash
textField.setText("New Text");
```

JTextField also supports various events such as focus events and action events. You can register event listeners to respond to these events. For example, to listen for changes to the text in the text field, you can add a document listener like this:

```bash
textField.getDocument().addDocumentListener(new DocumentListener() {
    @Override
    public void insertUpdate(DocumentEvent e) {
        // handle text insertion
    }

    @Override
    public void removeUpdate(DocumentEvent e) {
        // handle text removal
    }

    @Override
    public void changedUpdate(DocumentEvent e) {
        // handle text change
    }
});
```

Overall, JTextField is a powerful component in Java Swing that allows for flexible text editing and user input in GUI applications.
