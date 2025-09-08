Python ve discord.py kütüphanesi kullanılarak geliştirilmiş, YouTube gibi kaynaklardan müzik çalabilen gelişmiş bir Discord müzik botu. Hem ! prefix komutlarını hem de modern / slash komutlarını destekler.

✨ Özellikler
İsimle veya URL ile Müzik Çalma: YouTube linki veya direkt şarkı adıyla arama yaparak müzik çalar.

Çift Komut Desteği: Hem geleneksel !play gibi prefix komutlarını, hem de Discord'un yeni nesil /play gibi slash komutlarını destekler.

Sıraya Ekleme (Queue): Bir şarkı çalarken eklenen yeni şarkıları otomatik olarak sıraya alır.

Asenkron ve Donmayan Yapı: Şarkı arama gibi yavaş işlemler botu kilitlemez, bu sayede bot her zaman akıcı ve duyarlı kalır.

Kolay Kurulum ve Kullanım: Temel komutlarla (katıl, ayrıl, çal, durdur) kolayca yönetilebilir.

⚙️ Gereksinimler
Bu botu çalıştırabilmek için sisteminizde aşağıdakilerin kurulu olması gerekir:

Python 3.8 veya üstü

FFmpeg: Ses dosyalarını işlemek için zorunludur. Sistemin PATH (yol) değişkenine eklenmiş olmalıdır. FFmpeg İndirme Sayfası

Discord Bot Token: Discord Developer Portal üzerinden alınmış bir bot token'ı.

🚀 Kurulum
Proje Dosyalarını İndirin:
Bu projenin dosyalarını bilgisayarınıza indirin veya git clone ile klonlayın.

Proje Klasörüne Gidin:
Terminali açın ve proje klasörünün içine girin.

Bash

cd /path/to/DiscordMusicBot
Sanal Ortam (Virtual Environment) Oluşturun:
Kütüphaneleri sisteminizden izole bir şekilde kurmak için bir sanal ortam oluşturun.

Bash

python -m venv venv
Sanal Ortamı Aktif Edin:

Windows (PowerShell):

PowerShell

# Betik çalıştırma politikasını ayarlamanız gerekebilir (bir kerelik)
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process

# Aktif etme
.\venv\Scripts\Activate.ps1
macOS / Linux:

Bash

source venv/bin/activate
Aktif ettiğinizde komut satırının başında (venv) yazısını görmelisiniz.

Gerekli Kütüphaneleri Yükleyin:
Proje için gerekli olan Python kütüphanelerini requirements.txt dosyası ile yükleyin.

Bash

pip install -r requirements.txt
Eğer requirements.txt dosyanız yoksa, aşağıdaki komutla kütüphaneleri direkt kurabilirsiniz:

Bash

pip install discord.py yt-dlp PyNaCl
🛠️ Yapılandırma
Botu çalıştırabilmek için Discord bot token'ınızı kodun içine eklemeniz gerekmektedir.

main.py dosyasını bir metin düzenleyici ile açın.

Dosyanın en altındaki satırı bulun:

Python

bot.run('YOUR_BOT_TOKEN')
YOUR_BOT_TOKEN kısmını kendi bot token'ınız ile değiştirin.

⚠️ Uyarı: Bot token'ınızı kimseyle paylaşmayın! Bu, botunuzun kontrolünü başkasına vermek demektir.

▶️ Kullanım
Botu çalıştırmak için, sanal ortamınız aktifken terminale aşağıdaki komutu yazın:

Bash

python main.py
Bot başarıyla giriş yaptığında terminalde bir "giriş yapıldı" mesajı göreceksiniz.

Komutlar
Prefix Komutu	Slash Komutu	Açıklama
!join	/join	Botu bulunduğunuz ses kanalına çağırır.
!play <şarkı adı veya URL>	/play search:<şarkı adı veya URL>	Belirtilen şarkıyı çalar veya sıraya ekler.
!stop	/stop	Müziği tamamen durdurur ve sırayı temizler.
!leave	/leave	Botu ses kanalından ayırır.
