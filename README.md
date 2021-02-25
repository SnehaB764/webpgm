using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
 
namespace Program1
{
   public partial class _Default : System.Web.UI.Page
   {
       protected void Button1_Click(object sender, EventArgs e)
       {
           if (DropDownList1.SelectedIndex == 0 && DropDownList2.SelectedIndex == 1)
           {
               float cr = (float)(Convert.ToDouble(TextBox1.Text) * 74);
               Label5.Text = "Rs " + Convert.ToString(cr);
           }
           else if (DropDownList1.SelectedIndex == 1 && DropDownList2.SelectedIndex == 0)
           {
               float cr = (float)(Convert.ToDouble(TextBox1.Text) / 74);
               Label5.Text = "$ " + Convert.ToString(cr);
           }
           else
           {
               if (DropDownList1.SelectedIndex == 0)
                   Label5.Text = "$ " + TextBox1.Text;
               else
                   Label5.Text = "Rs " + TextBox1.Text;
           }
       }
   }
}
 
