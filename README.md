import java.awt.*;
import java.awt.event.*;

class studentMarks {
    public static void main(String[] args) {
        Frame f = new Frame("Students marks form");
        f.setSize(500,550); 
        f.setLayout(null); 
        f.setVisible(true);

        Label l = new Label("PLEASE FILL THIS FORM TO CALCULATE SUDENTS MARKS");
        l.setBounds(65, 40, 350,30);
        f.add(l);
        
        Label l1 = new Label("MATHIMATICS /30 : ");
        l1.setBounds(65, 80, 120,30);
        f.add(l1);
        TextField Tf1 = new TextField();
        Tf1.setBounds(200,80,190,30);
        f.add(Tf1);
        
        Label l2 = new Label("CHEMISTRY /30 : ");
        l2.setBounds(65, 120, 120,30);
        f.add(l2);
        TextField Tf2 = new TextField();
        Tf2.setBounds(200,120,190,30);
        f.add(Tf2);
        
        Label l3 = new Label("BIOLOGY /30 : ");
        l3.setBounds(65, 160, 120,30);
        f.add(l3);
        TextField Tf3 = new TextField();
        Tf3.setBounds(200,160,190,30);
        f.add(Tf3);
        
        Label l4 = new Label("PHYSICS /30 : ");
        l4.setBounds(65, 200, 120,30);
        f.add(l4);
        TextField Tf4 = new TextField();
        Tf4.setBounds(200,200,190,30);
        f.add(Tf4);
        
        Label l5 = new Label("DISPLAY ALL MARKS HERE : ");
        l5.setBounds(65, 240, 180,30);
        f.add(l5);
        TextField Tf5 = new TextField();
        Tf5.setBounds(250,240,140,30);
        f.add(Tf5);        
        
        Button b1 = new Button("PERCENTAGE");
        b1.setBounds(65, 280, 100, 30);
        f.add(b1);
        
        Button b2 = new Button("TOTAL");
        b2.setBounds(178, 280, 100, 30);
        f.add(b2);
        
        Button b3 = new Button("AVERAGE");
        b3.setBounds(290, 280, 100, 30);
        f.add(b3);

        Button b6 = new Button("CLICK TO CHECK GRADES");
        b6.setBounds(65, 330, 180,30);
        f.add(b6);
        TextField Tf6 = new TextField();
        Tf6.setBounds(250,330,140,30);
        f.add(Tf6); 

        b1.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e){
                Double num1 = Double.parseDouble(Tf1.getText());
                Double num2 = Double.parseDouble(Tf2.getText());
                Double num3 = Double.parseDouble(Tf3.getText());
                Double num4 = Double.parseDouble(Tf4.getText());
                Double percentage = (num1 + num2 + num3 + num4)/120 * 100;

                Tf5.setText(String.valueOf(percentage));
            }
        });
        b2.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e){
                Double num1 = Double.parseDouble(Tf1.getText());
                Double num2 = Double.parseDouble(Tf2.getText());
                Double num3 = Double.parseDouble(Tf3.getText());
                Double num4 = Double.parseDouble(Tf4.getText());
                Double result = num1 + num2 + num3 + num4;

                Tf5.setText(String.valueOf(result));
            }
        });
        b3.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e){
                Double num1 = Double.parseDouble(Tf1.getText());
                Double num2 = Double.parseDouble(Tf2.getText());
                Double num3 = Double.parseDouble(Tf3.getText());
                Double num4 = Double.parseDouble(Tf4.getText());
                Double result = (num1 + num2 + num3 + num4)/4;

                Tf5.setText(String.valueOf(result));
            }
        });
        b6.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e){
                Double num1 = Double.parseDouble(Tf1.getText());
                Double num2 = Double.parseDouble(Tf2.getText());
                Double num3 = Double.parseDouble(Tf3.getText());
                Double num4 = Double.parseDouble(Tf4.getText());
                Double percentage = (num1 + num2 + num3 + num4)/120 * 100;
                
                if (percentage <= 100 && percentage >= 80) {
                    Tf6.setText(String.valueOf("A"));
                } else if ( percentage < 80  && percentage >= 70) {
                    Tf6.setText(String.valueOf("B"));
                } else if (percentage < 70 && percentage >= 50) {
                    Tf6.setText(String.valueOf("C"));
                } else if (percentage < 50){
                    Tf6.setText(String.valueOf("Failed"));
                }else{
                    Tf6.setText(String.valueOf("Please Enter a valid number..."));
                }
            }
        });
    }
}


<!---
Abdallah319/Abdallah319 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
