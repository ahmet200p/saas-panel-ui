"Bayi portalında Dashboard, Siparişler, Ürünler gibi menülerde gezinirken, backend'e giden veri çekme (fetch) istekleri 400 Bad Request hatası alıyor. Ağ (Network) sekmesinde bu isteklerin api.js (satır 1761 civarı) üzerinden yapıldığı görülüyor.

api.js dosyasındaki merkezi API çağrı fonksiyonunu (fetch/axios interceptor) kontrol et.

Backend'e giden tüm isteklerin (GET, POST vb.) headers kısmına kullanıcının giriş yaparken aldığı Authorization (Bearer token) ve gerekiyorsa Tenant-ID (veya subdomain) bilgisinin dinamik ve doğru bir şekilde eklendiğinden emin ol.

Listeleme isteklerinde backend'in beklediği zorunlu sayfalama (pagination) veya filtre parametreleri varsa, bunların URL'e doğru eklendiğini kontrol et."