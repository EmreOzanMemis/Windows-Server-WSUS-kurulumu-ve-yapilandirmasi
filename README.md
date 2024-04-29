# Windows Server WSUS kurulumu ve yapilandirmasi
<div>Windows Server 2019 Windows Server Update Services (WSUS) kurulumu gerçekleştirerek yapınızda bulunan client ve server işletim sistemlerinizi güncelleyebilir güncelleme durumlarını görüntüleyebilir. Hangi server yada client işletim sisteminizde eksik güncelleme
        olduğunu takip edebilrisiniz. <br>
        </div>
        <div><br>
        </div>
        <div>WSUS yapısının kurgunuzu domain ortamında yada stand alone olarak yapabilirsiniz. WSUS ile yapınızda size ait Microsoft güncelleme sunucusu gibi konumlanmaktadır. Çoklu server ve client işletim sistemine sahip yapılarda internet kullanımını ve güncelleme
        takibini kolaylaştıran bu service ile bir kullanıcınızın işletim sisteminde başlattığı güncelleme sonrası internet ortamınzıda oluşan saturasyonuda engellemiş olursunuz.
        <br>
        </div>
        <div><br>
        </div>
        <div>Özelikle orta ve küçük ölçekli kuruluşlarda bu sorun sıklıkla yaşanmaktadır. Bu tip durumlarda yapınızda kurguluyacağınız WSUS ile tüm client ve server işletim sistemlerinizin güncelleme ihtiyaçlarını karşılayabilirsiniz. Windows Server işletim sistemi
        üzerine tanımlayacağınız WSUS role için kurulum ve yapilandirma ayaralarını sizin ile paylaşacağım.
        <br>
        </div>
        <div><br>
        </div>
        <div>Kurulum ve yapilandirma işlemlerini Windows Server 2019 işletim sistemi üzerinde gerçekleştireceğim aynı işlemleri Windows Server 2016, Windows Server 2012 R2 ve Windows Server 2012 üzerinde de aynı adımlar ile gerçekleştirebilirsiniz. Kurulum için Windows
        Server 2019 işletim sistemimde "Server Manager" açıyorum. Dashboard dizininde bulunan "Add roles and features" adımını tıklıyoruz ve kurulum için işlemlere başlıyoruz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ1.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Before you begin" adımında next butonuna basarak devam ediyoruz. <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ2.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Select installation type" adımında "role-based or feature-based installation" seçiyoruz ve next butonuna basıyoruz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ3.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Select server roles" adımında "Windows Server Update Services" role buluyoruz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ4.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Select server roles" adımında "Windows Server Update Services" role seçimini yaptığımızda bize "add feature that are required for Windows server update services" penceresinde kurulum için gerekli diğer role ve features listesini gösteriyor. Bu bölümde
        dikkat etmeniz gereken alt bölümde bulunan "Include management tools" opsiyonun seçili olmasıdır.</div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ5.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Seçim işlemlerimizi tamamladıktan sonra "select server roles" adımını next butonuna basarak geçiyoruz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ6.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Select features" adımında işlem yapmanıza gerek yoktur. Role seçimi sırasında ihtiyacımız olacak features otomatik olarak seçilmiştir. Next butonuna basarak devam edebiliriz.</div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ7.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"WSUS" adımında next butonuna basarak devam ediniz.</div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ8.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Select role services" adımında ilgili role servislerinin seçili olarak geldiğini göreceksiniz. Next butonuna basarak devam ediniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ9.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Content location selection" adımında WSUS tarafından indirilecek güncelleme paketleri için bir dizin belirtmeniz istenecektir. Sizin için uygun bir path belirterek next butonua basıp devam ediniz.</div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ10.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Web Server Role (IIS) adımında işlem yapmanıza gerek yoktur bu role kurulmasının sebebi WSUS raporlama servisinin alt yapısı IIS üzerinde çalıştığı içindir. Next butonuna basarak devam edebiliriz.</div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ11.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Select role services" adımında WSUS için gerekli olan web server roles and features zaten seçili gelecektir. Next butonuna basarak devam ediniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ12.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Confirm installation selections" adımında özetimizi görüntülüyoruz. "Restart the destination server automatically if requşred" seçeneğini işaretleyiniz. Bu işlem ile kurulum sırasında yada kurulum sonrası restart gerekirse sistem otomatik olarak gerçekleştirip
        sürece devam edecektir. <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ13.png">
        <img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ14.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Yükleme sırasında sistem reboot gerçekleşebilir endişe etmeyin reboot sonrası kurulum devam edecektir.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ15.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Yükleme işlemi bittikten sonra Start-&gt; administrative tools -&gt; Windows Server Update Services uygulamasını çalıştırınız.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ16.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>WSUS yapılandırma işlemleri için karşımıza Configuration wizard penceresi gelecektir. "Before you begin" adımında next butonuna başararak devam ediniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ17.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Microsoft update improvement program" adımında next butonuna basarak devam ediniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ18.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Choose Upstream server" adımında sync durumunu yapı ve kullanım şeklinize göre yapılandırabilirsiniz. Yapınızda başka bir wsus var ise SYNC from onether WSUS seçebilirsiniz. Eğer yapınızda ilk WSUS kurulumunuz ise SYNC from Microsoft Update seçmeniz gerekmektedir.
        Next butonuna basarak devam ediniz. <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ19.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Specify Proxy Server adımında yapınızda Proxy kullanıyorsanız bilgilerini giriniz kullanmıyorsanız next butonuna basarak devam ediniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ20.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Start Connecting butonuna basınız. İlgili ürün, dil ve güncellemeler için bağlantı işlemini gerçekleştiriniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ21.png"><br>
        </div>
        <div><br>
        </div>
        <div>Bağlantı işlemi biraz zaman alabilir.</div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ22.png"><br>
        </div>
        <div><br>
        </div>
        <div>Bağlantı işleminiz tamamlandıktan sonra next butonuna basarak devam ediniz. <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ23.png"><br>
        </div>
        <div><br>
        </div>
        <div>"Choose Languages" adımında güncelleme paketlerinde istediğiniz dilleri seçiniz ve next butonuna basarak devam ediniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ24.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Choose Productions" adımında ilgili işletim sistemleri, features ve ürünleri seçiniz. Next butonuna basarak devam ediniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ25.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Choose Classifications" adımında sync olmasını istediğiniz güncelleme paket türlerini seçiniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ26.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>"Configure SYNC Schedule" adımında sync süresini tanımlayınız. Next butonuna basarak devam ediniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ27.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Son olarak finished adımında finish butonuna basıp bitrebilirsiniz yada next butonuna basarak WSUS için gelen yenilikleri inceleyebilirsiniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ28.png"></div>
        <div><br>
        </div>
        <div>&nbsp;<img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ29.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Update services penceresinde size bir özet görüntü ve raporlamalar sunuclmuştur. İlk kurulum sonrası değerleri sıfır olarak göreceksiniz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ30.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>All updates adımında güncelleme paketlerini onaylamak için approval seçeneğini unapproval ve status bölümünü any olarak seçerek refresh ediyorum. İlgili güncelleme paketleri alt bölümde sıralanacaktır.</div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ31.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Onaylamak istediğim güncelleme paketlerini seçiyoruz ve Mouse sağ tuşu ile tıklayıp "approve" seçeneğini tıklıyoruz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ32.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Approved işleminin hangi computer gruplarına uygulanacağını seçerek izin veriyor ve ok butonuna basıyoruz.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ33.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Onaylama işlemi başlayacaktır. Onay verdiğiniz computer group ve inherit olarak uyguladığınız alt gruplara istinaden işlem biraz uzun sürebilir.
        <br>
        </div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ34.png"><br>
        </div>
        <div><br>
        </div>
        <div>İşlem tamamlandıktan sonra close butonuna basıyoruz. İlgili güncelleme paketleri download edilmeye başlayacaktır. Download işlemi otomatik yapılmaktadır. Disk kullanımını bu süreçte kontrol etmenizde fayda vardır. WSUS yapılandırma sırasında belirttiğiniz
        path üzerinden indirilen güncelleme paketlerini zaman içerisinde göreceksinizdir.</div>
        <div><br>
        </div>
        <div><img alt="" src="https://www.emreozanmemis.com/wp-content/uploads/2019/06/062119_0916_WindowsServ35.png">
        <br>
        </div>
        <div><br>
        </div>
        <div>Download işlemleri tamamlandığında approved olarak tanımladığınız güncelleme paketleri computer grouplarına eklediğiniz client yada server için hazır duruma gelecektir.
        <br>
        </div>
        <div><br>
        </div>
        <div><a href="https://social.technet.microsoft.com/wiki/contents/articles/53062.windows-update-servisini-wsus-olarak-yapilandirma-tr-tr.aspx">Computerlar WSUS üzerine nasıl eklenir merak ediyorsanız bu makaleyi inceleyiniz.</a></div>
        <div><br>
        </div>
        <div><a href="https://social.technet.microsoft.com/wiki/contents/articles/53060.powershell-ile-wsus-kurulumu-ve-yapilandirmasi-tr-tr.aspx">PowerShell ile WSUS kurulum ve yapılandırmasını incelemek için tıklayınız.
        <br>
        </a></div>
        <div><br>
        </div>
        <div>[View:https://www.youtube.com/watch?v=nnsIiMZdnCk&amp;t=267s] <br>
        </div>
