import java.awt.*;
import java.awt.event.*;
import javax.swing.*;
class BuildCalculator extends JFrame implements ActionListener{
 JFrame actualWindow;
 JPanel resultPanel, buttonPanel, infoPanel;
 JTextField resultTxt;
 JButton btn_digits[] = new JButton[10];
 JButton btn_plus, btn_minus, btn_mul, btn_div, btn_equal, btn_dot, btn_clear; 
 char eventFrom;
 JLabel expression, appTitle, siteTitle ;
 double oparand_1 = 0, operand_2 = 0;
 String operator = "=";
 BuildCalculator() {
 Font txtFont = new Font("SansSerif", Font.BOLD, 20);
 Font titleFont = new Font("SansSerif", Font.BOLD, 30)
 Font expressionFont = new Font("SansSerif", Font.BOLD, 15);
 actualWindow = new JFrame("Calculator");
 resultPanel = new JPanel();
 buttonPanel = new JPanel();
 infoPanel = new JPanel();
 actualWindow.setLayout(new GridLayout(3, 1));
 buttonPanel.setLayout(new GridLayout(4, 4));
 infoPanel.setLayout(new GridLayout(3, 1));
 actualWindow.setResizable(false);
 appTitle = new JLabel("My Calculator");
 appTitle.setFont(titleFont);
 expression = new JLabel("Expression shown here");
 expression.setFont(expressionFont);
 siteTitle = new JLabel("www.btechsmartclass.com");
 siteTitle.setFont(expressionFont);
 siteTitle.setHorizontalAlignment(SwingConstants.CENTER);
 siteTitle.setForeground(Color.BLUE);
 resultTxt = new JTextField(15);
 resultTxt.setBorder(null);
 resultTxt.setPreferredSize(new Dimension(15, 50));
 resultTxt.setFont(txtFont);
 resultTxt.setHorizontalAlignment(SwingConstants.RIGHT);
 for(int i = 0; i < 10; i++) {
 btn_digits[i] = new JButton(""+i);
