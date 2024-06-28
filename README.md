//form3
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace ÖDEV
{
    public partial class Form3 : Form
    {
        private Form4 form4;
        public Form3()
        {
            InitializeComponent();
        }
        bool tiklandi1 = false;
        bool tiklandi2 = false;
        bool tiklandi3 = false;
        bool tiklandi4 = false;
        bool tiklandi5 = false;
        bool tiklandi6 = false;
        bool tiklandi7 = false;
        bool tiklandi8 = false;
        bool tiklandi9 = false;
        bool ilktik = false;
        int hak = 5;
        private void tiklanma()
        {
            tiklandi1 = false;
            tiklandi2 = false;
            tiklandi3 = false;
            tiklandi4 = false;
            tiklandi5 = false;
            tiklandi6 = false;
            tiklandi7 = false;
            tiklandi8 = false;
            tiklandi9 = false;
        }
        private void sifirla()
        {
            pictureBox1.Image = null;
            pictureBox2.Image = null;
            pictureBox3.Image = null;
            pictureBox4.Image = null;
            pictureBox5.Image = null;
            pictureBox6.Image = null;
            pictureBox7.Image = null;
            pictureBox8.Image = null;
            pictureBox9.Image = null;
        }
        private void cozum()
        {
            if (ilktik == false)
            {
                ilktik = true;
                return;
            }
            if (tiklandi2 && tiklandi9 && !tiklandi1 && !tiklandi3 && !tiklandi4 && !tiklandi5 && !tiklandi6 && !tiklandi7 && !tiklandi8)
            {
                pictureBox2.Visible = false;
                pictureBox9.Visible = false;
                sifirla();
                tiklanma();
            }
            else if (tiklandi3 && tiklandi6 && !tiklandi1 && !tiklandi4 && !tiklandi5 && !tiklandi2 && !tiklandi7 && !tiklandi8 && !tiklandi9)
            {
                pictureBox3.Visible = false;
                pictureBox6.Visible = false;
                sifirla();
                tiklanma();
            }
            else if (tiklandi5 && tiklandi7 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi6 && !tiklandi8 && !tiklandi9)
            {
                pictureBox5.Visible = false;
                pictureBox7.Visible = false;
                sifirla();
                tiklanma();
            }
            else if (tiklandi4 && tiklandi8 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi5 && !tiklandi6 && !tiklandi7 && !tiklandi9)
            {
                pictureBox4.Visible = false;
                pictureBox8.Visible = false;
                sifirla();
                tiklanma();
            }
            else
            {
                hak--;
                if (hak > 0)
                {
                    MessageBox.Show("YANLIŞ SEÇİM YAPTINIZ. " + hak + " HAKKINIZ KALMIŞTIR");
                }
                sifirla();
                tiklanma();
                if (hak == 0)
                {
                    DialogResult cevap = MessageBox.Show("Oyunu kaybettiniz,LEVEL 1'e yeniden başlamak ister misiniz?", "?", MessageBoxButtons.YesNo, MessageBoxIcon.Question);
                    if (cevap == DialogResult.Yes)
                    {
                        pictureBox1.Visible = true;
                        pictureBox2.Visible = true;
                        pictureBox3.Visible = true;
                        pictureBox4.Visible = true;
                        pictureBox5.Visible = true;
                        pictureBox6.Visible = true;
                        pictureBox7.Visible = true;
                        pictureBox8.Visible = true;
                        pictureBox9.Visible = true;
                        hak = 5;
                        sifirla();
                        tiklanma();
                    }
                    else
                    {
                        Application.Exit();
                    }
                }
            }
            ilktik = false;
        }
        private void pictureBox1_Click(object sender, EventArgs e)
        {
            tiklandi1 = true;
            string dosya1 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\resimler\\etliekmek.jpeg";
            pictureBox1.Image = Image.FromFile(dosya1);
            cozum();
        }

        private void pictureBox2_Click(object sender, EventArgs e)
        {
            tiklandi2 = true;
            string dosya2 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\resimler\\ananas.jpeg";
            pictureBox2.Image = Image.FromFile(dosya2);
            cozum();
        }

        private void pictureBox9_Click(object sender, EventArgs e)
        {
            tiklandi9 = true;
            string dosya3 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\resimler\\ananas.jpeg";
            pictureBox9.Image = Image.FromFile(dosya3);
            cozum();
        }

        private void pictureBox3_Click(object sender, EventArgs e)
        {
            tiklandi3 = true;
            string dosya4 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\resimler\\çilek.jpeg";
            pictureBox3.Image = Image.FromFile(dosya4);
            cozum();
        }

        private void pictureBox6_Click(object sender, EventArgs e)
        {
            tiklandi6 = true;
            string dosya5 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\resimler\\çilek.jpeg";
            pictureBox6.Image = Image.FromFile(dosya5);
            cozum();
        }

        private void pictureBox5_Click(object sender, EventArgs e)
        {
            tiklandi5 = true;
            string dosya6 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\resimler\\avakado.jpeg";
            pictureBox5.Image = Image.FromFile(dosya6);
            cozum();
        }

        private void pictureBox4_Click(object sender, EventArgs e)
        {
            tiklandi4 = true;
            string dosya8 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\resimler\\kiraz.jpeg";
            pictureBox4.Image = Image.FromFile(dosya8);
            cozum();

        }

        private void pictureBox7_Click(object sender, EventArgs e)
        {
            tiklandi7 = true;
            string dosya7 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\resimler\\avakado.jpeg";
            pictureBox7.Image = Image.FromFile(dosya7);
            cozum();
        }

        private void pictureBox8_Click(object sender, EventArgs e)
        {
            tiklandi8 = true;
            string dosya9 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\resimler\\kiraz.jpeg";
            pictureBox8.Image = Image.FromFile(dosya9);
            cozum();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            if(!pictureBox3.Visible && !pictureBox2.Visible && !pictureBox4.Visible && !pictureBox5.Visible && !pictureBox6.Visible && !pictureBox7.Visible && !pictureBox8.Visible && !pictureBox9.Visible && pictureBox1.Visible)
            {
                if (tiklandi1 == true)
                {
                    form4.Show();
                    this.Hide();
                }
                else
                {
                    MessageBox.Show("SON KAREYE ULAŞMADAN SORUYU GÖREMEZSİNİZ");
                }
            }
            else
            {
                MessageBox.Show("SON KAREYE ULAŞMADAN SORUYU GÖREMEZSİNİZ.");
            }
        }

        private void Form3_Load(object sender, EventArgs e)
        {
            form4 = new Form4();

        }
    }
}

///FORM4
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace ÖDEV
{
    public partial class Form4 : Form
    {
        Form1 form1=new Form1();
        public Form4()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            string sehir;
            sehir = Convert.ToString(textBox1.Text);
            if(sehir=="konya" || sehir=="KONYA" || sehir == "Konya")
            {
              DialogResult cevap=  MessageBox.Show("DOĞRU BİLDİNİZ.TEBRİKLER. LEVEL2'YE GEÇMEK İSTER MİSİNİZ ?","?",MessageBoxButtons.YesNo,MessageBoxIcon.Question);
                if(cevap==DialogResult.Yes)
                {
                    form1.Show();
                    this.Hide();
                }
                else
                {
                    Application.Exit();
                }
            }
            else
            {
                MessageBox.Show("CEVAP 'KONYA' OLACAKTI KAYBETTİNİZ.");
                Application.Exit();
            }

        }
    }
}
///FORM1
using System;
using System.Windows.Forms;
namespace ÖDEV
{
    public partial class Form1 : Form
    {
        private Form2 form2;

        public Form1()
        {
            InitializeComponent();
        }
        int hak = 15;
        bool ilktik = false;
        bool tiklandi1 = false;
        bool tiklandi2 = false;
        bool tiklandi3 = false;
        bool tiklandi4 = false;
        bool tiklandi5 = false;
        bool tiklandi6 = false;
        bool tiklandi7 = false;
        bool tiklandi8 = false;
        bool tiklandi9 = false;
        bool tiklandi10 = false;
        bool tiklandi11 = false;
        bool tiklandi12 = false;
        bool tiklandi13 = false;
        bool tiklandi14 = false;
        bool tiklandi15 = false;
        bool tiklandi16 = false;
        bool tiklandi17 = false;
        bool tiklandi18 = false;
        bool tiklandi19 = false;
        bool tiklandi20 = false;
        bool tiklandi21 = false;
        bool tiklandi22 = false;
        bool tiklandi23 = false;
        bool tiklandi24 = false;
        bool tiklandi25 = false;
        private void tiklanma()
        {
            tiklandi1 = false;
            tiklandi2 = false;
            tiklandi3 = false;
            tiklandi4 = false;
            tiklandi5 = false;
            tiklandi6 = false;
            tiklandi7 = false;
            tiklandi8 = false;
            tiklandi9 = false;
            tiklandi10 = false;
            tiklandi11 = false;
            tiklandi12 = false;
            tiklandi13 = false;
            tiklandi14 = false;
            tiklandi15 = false;
            tiklandi16 = false;
            tiklandi17 = false;
            tiklandi18 = false;
            tiklandi19 = false;
            tiklandi20 = false;
            tiklandi21 = false;
            tiklandi22 = false;
            tiklandi23 = false;
            tiklandi24 = false;
            tiklandi25 = false;
        }
        private void sifirlanma()
        {
            pictureBox1.Image = null;
            pictureBox2.Image = null;
            pictureBox3.Image = null;
            pictureBox4.Image = null;
            pictureBox5.Image = null;
            pictureBox6.Image = null;
            pictureBox7.Image = null;
            pictureBox8.Image = null;
            pictureBox9.Image = null;
            pictureBox10.Image = null;
            pictureBox11.Image = null;
            pictureBox12.Image = null;
            pictureBox13.Image = null;
            pictureBox14.Image = null;
            pictureBox15.Image = null;
            pictureBox16.Image = null;
            pictureBox17.Image = null;
            pictureBox18.Image = null;
            pictureBox19.Image = null;
            pictureBox20.Image = null;
            pictureBox21.Image = null;
            pictureBox22.Image = null;
            pictureBox23.Image = null;
            pictureBox24.Image = null;
            pictureBox25.Image = null;
        }

        private void cozum()
        {
            if (ilktik == false)
            {
               ilktik = true;
                return;
           }
            if (tiklandi1 && tiklandi19 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi5 && !tiklandi6 && !tiklandi7 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi14 && !tiklandi15 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi20 && !tiklandi21 && !tiklandi22 && !tiklandi23 && !tiklandi24 && !tiklandi25)
            {
                pictureBox1.Visible = false;
                pictureBox19.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi10 && tiklandi8 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi5 && !tiklandi6 && !tiklandi7 && !tiklandi9 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi14 && !tiklandi15 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi20 && !tiklandi21 && !tiklandi22 && !tiklandi23 && !tiklandi24 && !tiklandi25)
            {
                pictureBox10.Visible = false;
                pictureBox8.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi15 && tiklandi5 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi14 && !tiklandi6 && !tiklandi7 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi20 && !tiklandi21 && !tiklandi22 && !tiklandi23 && !tiklandi24 && !tiklandi25)
            {
                pictureBox5.Visible = false;
                pictureBox15.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi20 && tiklandi11 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi14 && !tiklandi6 && !tiklandi7 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi5 && !tiklandi12 && !tiklandi13 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi15 && !tiklandi21 && !tiklandi22 && !tiklandi23 && !tiklandi24 && !tiklandi25)
            {
                pictureBox20.Visible = false;
                pictureBox11.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi25 && tiklandi6 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi14 && !tiklandi15 && !tiklandi7 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi20 && !tiklandi21 && !tiklandi22 && !tiklandi23 && !tiklandi24 && !tiklandi5)
            {
                pictureBox25.Visible = false;
                pictureBox6.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi2 && tiklandi23 && !tiklandi1 && !tiklandi5 && !tiklandi3 && !tiklandi4 && !tiklandi14 && !tiklandi6 && !tiklandi7 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi20 && !tiklandi21 && !tiklandi22 && !tiklandi15 && !tiklandi24 && !tiklandi25)
            {
                pictureBox2.Visible = false;
                pictureBox23.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi9 && tiklandi16 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi14 && !tiklandi6 && !tiklandi7 && !tiklandi8 && !tiklandi5 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi15 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi20 && !tiklandi21 && !tiklandi22 && !tiklandi23 && !tiklandi24 && !tiklandi25)
            {
                pictureBox9.Visible = false;
                pictureBox16.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi14 && tiklandi22 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi5 && !tiklandi6 && !tiklandi7 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi20 && !tiklandi21 && !tiklandi15 && !tiklandi23 && !tiklandi24 && !tiklandi25)
            {
                pictureBox22.Visible = false;
                pictureBox14.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi3 && tiklandi24 && !tiklandi1 && !tiklandi2 && !tiklandi5 && !tiklandi4 && !tiklandi14 && !tiklandi6 && !tiklandi7 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi20 && !tiklandi21 && !tiklandi22 && !tiklandi23 && !tiklandi15 && !tiklandi25)
            {
                pictureBox3.Visible = false;
                pictureBox24.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi13 && tiklandi21 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi14 && !tiklandi6 && !tiklandi7 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi5 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi20 && !tiklandi15 && !tiklandi22 && !tiklandi23 && !tiklandi24 && !tiklandi25)
            {
                pictureBox13.Visible = false;
                pictureBox21.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi17 && tiklandi18 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi4 && !tiklandi14 && !tiklandi6 && !tiklandi7 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi16 && !tiklandi5 && !tiklandi15 && !tiklandi19 && !tiklandi20 && !tiklandi21 && !tiklandi22 && !tiklandi23 && !tiklandi24 && !tiklandi25)
            {
                pictureBox17.Visible = false;
                pictureBox18.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else if (tiklandi4 && tiklandi7 && !tiklandi1 && !tiklandi2 && !tiklandi3 && !tiklandi5 && !tiklandi14 && !tiklandi6 && !tiklandi15 && !tiklandi8 && !tiklandi9 && !tiklandi10 && !tiklandi11 && !tiklandi12 && !tiklandi13 && !tiklandi16 && !tiklandi17 && !tiklandi18 && !tiklandi19 && !tiklandi20 && !tiklandi21 && !tiklandi22 && !tiklandi23 && !tiklandi24 && !tiklandi25)
            {
                pictureBox4.Visible = false;
                pictureBox7.Visible = false;
                sifirlanma();
                tiklanma();
            }
            else
            {
                hak--;
                if (hak > 0)
                {
                    MessageBox.Show("YANLIŞ SEÇİM YAPTINIZ. " + hak + " HAKKINIZ KALMIŞTIR.");
                }
                sifirlanma();
                tiklanma();

                if (hak == 0)
                {
                    DialogResult cevap = MessageBox.Show("Oyunu kaybettiniz,LEVEL 2'ye yeniden başlamak ister misiniz?", "?", MessageBoxButtons.YesNo, MessageBoxIcon.Question);
                    if (cevap == DialogResult.Yes)
                    {
                        pictureBox1.Visible = true;
                        pictureBox2.Visible = true;
                        pictureBox3.Visible = true;
                        pictureBox4.Visible = true;
                        pictureBox5.Visible = true;
                        pictureBox6.Visible = true;
                        pictureBox7.Visible = true;
                        pictureBox8.Visible = true;
                        pictureBox9.Visible = true;
                        pictureBox10.Visible = true;
                        pictureBox11.Visible = true;
                        pictureBox12.Visible = true;
                        pictureBox13.Visible = true;
                        pictureBox14.Visible = true;
                        pictureBox15.Visible = true;
                        pictureBox16.Visible = true;
                        pictureBox17.Visible = true;
                        pictureBox18.Visible = true;
                        pictureBox19.Visible = true;
                        pictureBox20.Visible = true;
                        pictureBox21.Visible = true;
                        pictureBox22.Visible = true;
                        pictureBox23.Visible = true;
                        pictureBox24.Visible = true;
                        pictureBox25.Visible = true;
                        hak = 15;
                        sifirlanma();
                        tiklanma();
                    }
                    else
                    {
                        Application.Exit();
                    }
                }
            }
            ilktik = false;
        }






        private void pictureBox1_Click(object sender, EventArgs e)
        {
            tiklandi1 = true;
            string dosya1 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\corba.jpeg";
            pictureBox1.Image = Image.FromFile(dosya1);
            cozum();

        }

        private void pictureBox10_Click(object sender, EventArgs e)
        {
            tiklandi10 = true;
            string dosya2 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\fuse tea.jpeg";
            pictureBox10.Image = Image.FromFile(dosya2);
            cozum();
        }

        private void pictureBox15_Click(object sender, EventArgs e)
        {
            tiklandi15 = true;
            string dosya3 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\hot dog.jpeg";
            pictureBox15.Image = Image.FromFile(dosya3);
            cozum();
        }

        private void pictureBox20_Click(object sender, EventArgs e)
        {
            tiklandi20 = true;
            string dosya4 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\inek.jpeg";
            pictureBox20.Image = Image.FromFile(dosya4);
            cozum();
        }

        private void pictureBox25_Click(object sender, EventArgs e)
        {
            tiklandi25 = true;
            string dosya5 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\kopek.jpeg";
            pictureBox25.Image = Image.FromFile(dosya5);
            cozum();
        }

        private void pictureBox2_Click(object sender, EventArgs e)
        {
            tiklandi2 = true;
            string dosya6 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\nar.jpeg";
            pictureBox2.Image = Image.FromFile(dosya6);
            cozum();
        }

        private void pictureBox9_Click(object sender, EventArgs e)
        {
            tiklandi9 = true;
            string dosya7 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\noodle.jpeg";
            pictureBox9.Image = Image.FromFile(dosya7);
            cozum();
        }

        private void pictureBox14_Click(object sender, EventArgs e)
        {
            tiklandi14 = true;
            string dosya8 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\fare.png";
            pictureBox14.Image = Image.FromFile(dosya8);
            cozum();
        }

        private void pictureBox19_Click(object sender, EventArgs e)
        {
            tiklandi19 = true;
            string dosya9 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\corba.jpeg";
            pictureBox19.Image = Image.FromFile(dosya9);
            cozum();

        }

        private void pictureBox24_Click(object sender, EventArgs e)
        {
            tiklandi24 = true;
            string dosya10 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\pizza.jpeg";
            pictureBox24.Image = Image.FromFile(dosya10);
            cozum();
        }

        private void pictureBox3_Click(object sender, EventArgs e)
        {
            tiklandi3 = true;
            string dosya11 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\pizza.jpeg";
            pictureBox3.Image = Image.FromFile(dosya11);
            cozum();
        }

        private void pictureBox8_Click(object sender, EventArgs e)
        {
            tiklandi8 = true;
            string dosya12 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\fuse tea.jpeg";
            pictureBox8.Image = Image.FromFile(dosya12);
            cozum();
        }

        private void pictureBox13_Click(object sender, EventArgs e)
        {
            tiklandi13 = true;
            string dosya13 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\su.jpeg";
            pictureBox13.Image = Image.FromFile(dosya13);
            cozum();
        }

        private void pictureBox17_Click(object sender, EventArgs e)
        {
            tiklandi17 = true;
            string dosya16 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\kola.jpeg";
            pictureBox17.Image = Image.FromFile(dosya16);
            cozum();
        }

        private void pictureBox21_Click(object sender, EventArgs e)
        {
            tiklandi21 = true;
            string dosya14 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\su.jpeg";
            pictureBox21.Image = Image.FromFile(dosya14);
            cozum();
        }

        private void pictureBox18_Click(object sender, EventArgs e)
        {
            tiklandi18 = true;
            string dosya15 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\kola.jpeg";
            pictureBox18.Image = Image.FromFile(dosya15);
            cozum();
        }

        private void pictureBox22_Click(object sender, EventArgs e)
        {
            tiklandi22 = true;
            string dosya19 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\fare.png";
            pictureBox22.Image = Image.FromFile(dosya19);
            cozum();
        }

        private void pictureBox5_Click(object sender, EventArgs e)
        {
            tiklandi5 = true;
            string dosya20 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\hot dog.jpeg";
            pictureBox5.Image = Image.FromFile(dosya20);
            cozum();
        }

        private void pictureBox6_Click(object sender, EventArgs e)
        {
            tiklandi6 = true;
            string dosya21 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\kopek.jpeg";
            pictureBox6.Image = Image.FromFile(dosya21);
            cozum();

        }

        private void pictureBox11_Click(object sender, EventArgs e)
        {
            tiklandi11 = true;
            string dosya22 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\inek.jpeg";
            pictureBox11.Image = Image.FromFile(dosya22);
            cozum();
        }

        private void pictureBox16_Click(object sender, EventArgs e)
        {
            tiklandi16 = true;
            string dosya23 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\noodle.jpeg";
            pictureBox16.Image = Image.FromFile(dosya23);
            cozum();
        }

        private void pictureBox23_Click(object sender, EventArgs e)
        {
            tiklandi23 = true;
            string dosya24 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\nar.jpeg";
            pictureBox23.Image = Image.FromFile(dosya24);
            cozum();
        }

        private void pictureBox4_Click(object sender, EventArgs e)
        {
            tiklandi4 = true;
            string dosya25 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\pasta.jpeg";
            pictureBox4.Image = Image.FromFile(dosya25);
            cozum();
        }

        private void pictureBox7_Click(object sender, EventArgs e)
        {
            tiklandi7 = true;
            string dosya26 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\pasta.jpeg";
            pictureBox7.Image = Image.FromFile(dosya26);
            cozum();
        }

        private void pictureBox12_Click(object sender, EventArgs e)
        {
            tiklandi12 = true;
            string dosya27 = "C:\\Users\\Esra\\source\\repos\\ÖDEV\\ÖDEV\\Properties\\fotograflar\\sucuk.jpeg";
            pictureBox12.Image = Image.FromFile(dosya27);
            cozum();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            form2 = new Form2();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            if (!pictureBox1.Visible && !pictureBox2.Visible && !pictureBox3.Visible && !pictureBox4.Visible && !pictureBox5.Visible && !pictureBox6.Visible && !pictureBox7.Visible && !pictureBox8.Visible && !pictureBox9.Visible && !pictureBox10.Visible && !pictureBox11.Visible && pictureBox12.Visible && !pictureBox13.Visible && !pictureBox14.Visible && !pictureBox15.Visible && !pictureBox16.Visible && !pictureBox17.Visible && !pictureBox18.Visible && !pictureBox19.Visible && !pictureBox20.Visible && !pictureBox21.Visible && !pictureBox22.Visible && !pictureBox23.Visible && !pictureBox24.Visible && !pictureBox25.Visible)
            {
                if (tiklandi12 == true)
                {
                    form2.Show();
                    this.Hide();
                }
                else
                {
                    MessageBox.Show("SON KAREYE ULAŞMADAN SORUYU GÖREMEZSİNİZ");
                }
            }
            else
            {
                MessageBox.Show("SON KAREYE ULAŞMADAN SORUYU GÖREMEZSİNİZ !");
            }
        }
    }
}
///FORM1
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace ÖDEV
{
    public partial class Form2 : Form
    {
        public Form2()
        {
            InitializeComponent();
        }
        string sehir;
 
        private void button1_Click(object sender, EventArgs e)
        {
            sehir=Convert.ToString(textBox1.Text);
            if(sehir=="AFYONKARAHİSAR" || sehir=="Afyonkarahisar" || sehir=="afyonkarahisar" || sehir=="afyon" || sehir=="AFYON")
            { 
                MessageBox.Show("OYUNU KAZANDINIZ.TEBRİKLER");
                Application.Exit();
            
            }
            else
            {
                MessageBox.Show("CEVAP AFYONKARAHİSARDI.OYUNU KAYBETTİNİZ.");
                Application.Exit();
            }
        }
    }
}

   
