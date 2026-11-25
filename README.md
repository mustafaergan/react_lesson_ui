# React + Redux Ders Projesi

React derslerinde adım adım geliştirilen örnek arayüz: React Router ile sayfa geçişleri, Redux + redux-thunk ile durum yönetimi ve axios ile servisten veri çekme.

> **Not:** Bu depo 2020 yılında eğitim/örnek amaçlı yazıldı ve artık güncellenmiyor. Bağımlılıkları eskidir ve bilinen güvenlik açıkları içerir; üretimde kullanmayın.

## İçerik

- `src/app.js` — giriş noktası: Redux store'u kurar, `/` (Dashboard) ve `/list` (SBMList) rotalarını tanımlar, açılışta örnek kullanıcı verisini jsonplaceholder'dan çeker.
- `src/components/` — `Header` (menü), `Dashboard`, `SBMList` (servisten gelen gönderim kayıtlarını tablo halinde gösterecek liste) ve `SBMRow`.
- `src/actions/actions.js` — yükleniyor durumu ve servisten veri çeken thunk aksiyonu (`/sendData/` ucunu çağırır).
- `src/reducers/`, `src/store/configureStore.js` — reducer'lar ve store yapılandırması.
- `webpack.config.js`, `.babelrc` — Babel (env + react preset) ile webpack derlemesi; çıktı `public/script.js`.

Proje ders sırasında yarım bırakılmıştır: `SBMList.js` içinde JSX etiketleri eşleşmediği için derleme bu dosyada hata verir; listeleme kısmı da yorum satırındadır.

## Teknolojiler

- React 16.12, React Router 5, Redux 4, React Redux 7, redux-thunk, axios
- Babel 7, webpack 4, webpack-dev-server 3

## Çalıştırma

1. `npm install`
2. `public` klasörüne `<div id="app"></div>` içeren ve `script.js` dosyasını yükleyen bir `index.html` ekleyin (depoda yoktur).
3. `npm run devServer` ile geliştirme sunucusunu başlatın ya da `npm run build:dev` ile `public/script.js` dosyasını üretip `npm run live` ile açın.
4. Liste sayfası verisini `src/actions/actions.js` içindeki `API_URL` adresindeki servisten alır; kendi servisinizin adresini yazın.
