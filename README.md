# C# ALAN HESABI
namespace WinFormsApp21
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            //KARE ALANI HESAPLAMA
            int kareKenar = Convert.ToInt32(textBoxKareKenar.Text);
           int kareAlan = kareKenar * kareKenar;
            textBoxAlanKare.Text = kareAlan.ToString();

            //DİKDORTGEN ALANI HESAPLAMA
            int kisaKenar = Convert.ToInt32(textBoxKisa.Text);
            int uzunKenar = Convert.ToInt32(textBoxUzun.Text);
            int dikdotgenAlan = kisaKenar * uzunKenar;
            textBoxAlanDikdortgen.Text = dikdotgenAlan.ToString();

            //DAİRE ALANI HESAPLAMA
            int yaricap = Convert.ToInt32(textBoxYaricap.Text);
            double daireAlan = Math.PI * yaricap * yaricap;
            textBoxAlanDaire.Text = daireAlan.ToString();
        }
    }
}
