# Esbo-o-de-IP-Tool-c-By-KaLi-_-LiNuX
Esboço de IP Tool c# By KaLi-_-LiNuX


     Esboço de IP Tool c# By KaLi-_-LiNuX



 private void Tracker_Click(object sender, EventArgs e)
        {
            outputbox.Text = this.wb.DownloadString(string.Format("http://ip-api.com/line/" + this.IPAddress.Text));
	}



public partial class Form1 : Form
    {

        private WebClient wb;
        public Form1()
        {
            wb = new WebClient();
            InitializeComponent();
        }



private void button7_Click(object sender, EventArgs e)
        {
            try
            {
                SaveFileDialog saveFileDialog = new SaveFileDialog();
                saveFileDialog.Filter = "Text Documents(*.txt)|*.txt|All Files(*.*)|*.*";
                saveFileDialog.Title = "Save Results";
                if (saveFileDialog.ShowDialog() == DialogResult.OK)
                    this.outputbox.SaveFile(saveFileDialog.FileName, RichTextBoxStreamType.PlainText);
                this.Text = saveFileDialog.FileName;

            }
            catch (Exception)
            {
                int num = (int)MessageBox.Show("Something went wrong :/", "ERROR", MessageBoxButtons.OK, MessageBoxIcon.Hand);
            }

        }



 private void Clear_Click(object sender, EventArgs e) => outputbox.Text = "";




 output1.Text = wb.DownloadString(string.Format("http://ipv4bot.whatismyipaddress.com/"));

