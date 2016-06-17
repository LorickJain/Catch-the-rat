import java.util.*;
import javax.swing.*;
import javax.swing.Timer;

import java.awt.*;
import java.awt.event.*;
public class CatchRat {
	private static Scanner sc;

	static void createframe(int k)
	{
	JFrame frame = new JFrame();
	frame.setTitle("RAT-CATCHER");
	frame.setSize(550,550);
	frame.setResizable(false);
	frame.setLayout(new FlowLayout());
	frame.getContentPane().setBackground(Color.green);
	frame.getContentPane().setLayout(new FlowLayout());
	JLabel lb;
	lb=new JLabel(new ImageIcon("C:/Users/loric/Desktop/player.png"));
	lb.setMinimumSize(new Dimension(40,40));
	lb.setPreferredSize(new Dimension(50,50));
	lb.setMaximumSize(new Dimension(60,60));
	
	frame.getContentPane().add(lb);
	Random r = new Random();
	 new Timer(k,new ActionListener(){
		  public void actionPerformed(ActionEvent ae)
		  {
			  lb.setLocation(r.nextInt(frame.getWidth()-75),r.nextInt(frame.getHeight()-75));
		  }
		 }).start();
	 lb.addMouseListener(new MouseAdapter(){
		 public void mouseClicked(MouseEvent me)
		  {
		  Toolkit.getDefaultToolkit().beep();
		  JOptionPane.showMessageDialog(null, "CAUGHT THE RAT");
		  frame.dispatchEvent(new WindowEvent(frame, WindowEvent.WINDOW_CLOSING));
		  }
		 });
	
	
	frame.setVisible(true);
	
	}

	public static  void main(String[] args)
	{
		sc = new Scanner(System.in);
		System.out.println("Enter the speed(an integer)");
		int x=sc.nextInt();
		createframe(x);
	}
}
