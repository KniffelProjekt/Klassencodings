# Klassencodings
import java.awt.BorderLayout;
import java.util.Arrays;
import java.util.Vector;

import javax.swing.JFrame;
import javax.swing.JScrollPane;
import javax.swing.JTable;
import javax.swing.table.TableColumn;
import java.awt.Font;
import java.awt.List;

public class tabelle {

public static void main(String args[]) {
    JFrame frame = new JFrame();
    frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

    Vector<String> rowOne = new Vector<String>();
    rowOne.addElement("1-er");
    
    Vector<String> rowTwo = new Vector<String>();
    rowTwo.addElement("2-er");
    
    Vector<String> rowThree = new Vector<String>();
    rowThree.addElement("3-er");
    
    Vector<String> rowFour = new Vector<String>();
    rowFour.addElement("4-er");
    
    Vector<String> rowFive = new Vector<String>();
    rowFive.addElement("5-er");
    
    Vector<String> rowSix = new Vector<String>();
    rowSix.addElement("6-er");
    
    Vector<String> rowSeven = new Vector<String>();
    rowSeven.addElement("Gesamt");
    
    Vector<String> rowEight = new Vector<String>();
    rowEight.addElement("Bonus(63+)");
    
    Vector<String> rowNine = new Vector<String>();
    rowNine.addElement("Gesamt (oben)");
    
    Vector<String> rowTen = new Vector<String>();
    rowTen.addElement("3-er Pasch");
    
    Vector<String> rowEleven = new Vector<String>();
    rowEleven.addElement("4-er Pasch");
    
    Vector<String> rowTwelve = new Vector<String>();
    rowTwelve.addElement("Full House");
    
    Vector<String> rowThirteen = new Vector<String>();
    rowThirteen.addElement("Kleine Straße");
    
    Vector<String> rowFourteen = new Vector<String>();
    rowFourteen.addElement("Große Straße");
    
    Vector<String> rowFifteen = new Vector<String>();
    rowFifteen.addElement("Kniffel");
    
    Vector<String> rowSixteen = new Vector<String>();
    rowSixteen.addElement("Chance");
    
    Vector<String> rowSeventeen = new Vector<String>();
    rowSeventeen.addElement("Gesamt (unten)");
    
    Vector<String> rowEighteen = new Vector<String>();
    rowEighteen.addElement("Gesamt (oben)");
    
    Vector<String> rowNineteen = new Vector<String>();
    rowNineteen.addElement("Endsumme");
    
    Vector<Vector> rowData = new Vector<Vector>();
    rowData.addElement(rowOne);
    rowData.addElement(rowTwo);
    rowData.addElement(rowThree);
    rowData.addElement(rowFour);
    rowData.addElement(rowFive);
    rowData.addElement(rowSix);
    rowData.addElement(rowSeven);
    rowData.addElement(rowEight);
    rowData.addElement(rowNine);
    rowData.addElement(rowTen);
    rowData.addElement(rowEleven);
    rowData.addElement(rowTwelve);
    rowData.addElement(rowThirteen);
    rowData.addElement(rowFourteen);
    rowData.addElement(rowFifteen);
    rowData.addElement(rowSixteen);
    rowData.addElement(rowSeventeen);
    rowData.addElement(rowEighteen);
    rowData.addElement(rowNineteen);
    
    String[] tmpcolumnNames = new String[9];    
   
    Vector<String> columnNamesV = new Vector<String>();  
    
    for(int i=0; i<=tmpcolumnNames.length -1; i++)
    {
        if(!(tmpcolumnNames[i] == null))
        {
        	columnNamesV.add(tmpcolumnNames[i]);
        }           
   }
    
    JTable table = new JTable(rowData, columnNamesV);
    table.setFont(new Font("Century Gothic", Font.PLAIN, 14));
    
    TableColumn columnName = null;
    for (int i = 0; i<columnNamesV.size(); i++) {
        columnName = table.getColumnModel().getColumn(i);
        if (i == 0) {
            columnName.setPreferredWidth(150); //third column is bigger
        } else {
            columnName.setPreferredWidth(75);
        }
    }
    
    table.setAutoResizeMode(JTable.AUTO_RESIZE_OFF);
    
    JScrollPane scrollPane = new JScrollPane(table);
    frame.getContentPane().add(scrollPane, BorderLayout.CENTER);
    frame.setVisible(true);

  }
}
 
