<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>見て・聴いて・叩いて楽しむ太鼓展！ - 浜田高校吹奏楽部</title>
    <!-- Tailwind CSSの読み込み --><script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* フォント設定 (日本語にも対応した視認性の高いフォント) */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&family=Noto+Sans+JP:wght@400;700&display=swap');
        body {
            font-family: 'Noto Sans JP', 'Inter', sans-serif;
            background-color: #f7f A7f7; /* 背景は少し明るいグレー */
        }
        .hero-section {
            background-color: #1a202c; /* ダークな背景でポスターの黒板のイメージを再現 */
            background-image: url('https://placehold.co/1200x600/1a202c/ffffff?text=BEAT+EXHIBITION');
            background-size: cover;
            background-position: center;
            position: relative;
        }
        .hero-section::before {
            /* ポスターの雰囲気に合わせたオーバーレイ */
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(26, 32, 44, 0.75);
        }
        .drum-card {
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            background-color: #ffffff;
        }
        .drum-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
        }
        .highlight-text {
            /* ポスターの黄色い文字をイメージ */
            color: #fca311;
            font-weight: 800;
        }
    </style>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'primary': '#dc2626', /* 赤色をメインカラーに */
                        'secondary': '#fca311', /* 黄色をハイライトに */
                        'dark-bg': '#1a202c',
                    },
                }
            }
        }
        
        // スムーススクロール
        document.addEventListener('DOMContentLoaded', () => {
            const links = document.querySelectorAll('a[href^="#"]');
            links.forEach(link => {
                link.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href').substring(1);
                    const targetElement = document.getElementById(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80, // 固定ヘッダーの分を考慮
                            behavior: 'smooth'
                        });
                    }
                });
            });
            
            // QRコード生成の処理は削除されました。
        });

        // 簡易的なお問い合わせメッセージ表示
        function showContactMessage() {
            const messageBox = document.getElementById('contact-message');
            messageBox.textContent = 'お問い合わせは 太鼓推進委員会 (0855-22-XXXX) までご連絡ください。'; // 問い合わせ先も仮で変更
            messageBox.classList.remove('hidden');
            setTimeout(() => {
                messageBox.classList.add('hidden');
            }, 5000);
        }
    </script>
</head>
<body class="bg-gray-50 text-gray-800">

    <!-- ナビゲーションバー (固定) --><header class="fixed top-0 left-0 right-0 bg-white shadow-md z-10">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="text-2xl font-bold text-primary">太鼓展！</div>
            <div class="hidden md:flex space-x-6">
                <a href="#about" class="text-gray-600 hover:text-primary transition duration-150">太鼓展とは</a>
                <a href="#drums" class="text-gray-600 hover:text-primary transition duration-150">展示・体験内容</a>
                <a href="#details" class="text-gray-600 hover:text-primary transition duration-150">開催概要</a>
                <a href="#access" class="text-gray-600 hover:text-primary transition duration-150">アクセス</a>
            </div>
            <button class="md:hidden text-gray-600 focus:outline-none">
                <!-- モバイルメニューアイコン (SVG) --><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
            </button>
        </nav>
    </header>

    <!-- ヒーローセクション --><section id="hero" class="hero-section text-white pt-32 pb-24 md:py-48 flex items-center justify-center">
        <div class="relative z-10 text-center px-4">
            <!-- サブタイトル --><p class="text-2xl sm:text-3xl mb-4 font-semibold text-secondary">太鼓推進委員会presents</p>
            <h1 class="text-6xl sm:text-8xl md:text-9xl font-extrabold tracking-tight mb-6" style="text-shadow: 4px 4px 6px rgba(0,0,0,0.8);">
                太鼓展！
            </h1>
            <h2 class="text-3xl sm:text-4xl md:text-5xl font-bold mb-10" style="text-shadow: 2px 2px 4px rgba(0,0,0,0.6);">
                <span class="highlight-text">見て・聴いて・叩いて</span>楽しむ！
            </h2>
            <div class="bg-white text-dark-bg p-6 rounded-xl inline-block shadow-2xl">
                <p class="text-xl md:text-2xl font-bold mb-2">日時: 11月11日（土）</p>
                <p class="text-lg md:text-xl font-medium">場所: 浜田高校 吹奏楽部室</p>
                <p class="text-3xl font-extrabold text-primary mt-4">入場無料！</p>
            </div>

            <!-- 申し込みボタン (トップ) --><div class="mt-12">
                <a href="https://docs.google.com/forms/d/e/1FAIpQLScPoAQWz6z7tLgch5pKRH5t3tkQE9VNBxU-seAffpTDkH9CKA/viewform?usp=header" target="_blank" class="inline-block bg-secondary text-dark-bg py-4 px-12 rounded-full text-2xl font-extrabold uppercase hover:bg-yellow-400 transition duration-300 shadow-xl transform hover:scale-105">
                    太鼓展に申し込む
                </a>
            </div>
            
        </div>
    </section>

    <!-- 太鼓展とは？セクション --><section id="about" class="py-16 md:py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 text-center">
            <h3 class="text-3xl font-bold text-gray-900 mb-4 border-b-4 border-primary inline-block pb-1">太鼓展とは？</h3>
            <p class="text-lg text-gray-600 mb-12">
                <!-- 説明文 -->いつもステージで活躍している打楽器の数々。あなたはそれらがどんな楽器で、どんな役割があるか知っていますか？<br class="hidden sm:inline">
                太鼓推進委員会が、パーカッションの魅力をもっと身近に感じてもらうために企画しました。
            </p>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- カード1: 見る --><div class="p-6 rounded-xl bg-gray-50 shadow-lg border-t-4 border-primary">
                    <div class="text-5xl mb-3 text-primary">👀</div>
                    <h4 class="text-xl font-semibold mb-2">【見る】世界の太鼓</h4>
                    <p class="text-gray-600">ポスターに描かれた様々な国の太鼓から、和太鼓まで。普段触れることのない楽器の歴史や構造を見て学べます。</p>
                </div>
                <!-- カード2: 聴く --><div class="p-6 rounded-xl bg-gray-50 shadow-lg border-t-4 border-secondary">
                    <div class="text-5xl mb-3 text-secondary">👂</div>
                    <h4 class="text-xl font-semibold mb-2">【聴く】デモンストレーション</h4>
                    <p class="text-gray-600">吹奏楽部員による、各太鼓の特徴的な音色や迫力ある演奏を間近で聴くことができます。質問コーナーもあります！</p>
                </div>
                <!-- カード3: 叩く --><div class="p-6 rounded-xl bg-gray-50 shadow-lg border-t-4 border-primary">
                    <div class="text-5xl mb-3 text-primary">🥁</div>
                    <h4 class="text-xl font-semibold mb-2">【叩く】体験コーナー</h4>
                    <p class="text-gray-600">プロのドラマー気分！実際に太鼓を叩いて、その振動と響きを感じてみましょう。部員が優しくレクチャーします。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 展示太鼓紹介セクション --><section id="drums" class="py-16 md:py-24 bg-gray-100">
        <div class="max-w-7xl mx-auto px-4">
            <h3 class="text-3xl font-bold text-center text-gray-900 mb-12 border-b-4 border-secondary inline-block pb-1">展示される主な太鼓</h3>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Drums (ドラム) --><div class="drum-card p-6 rounded-xl shadow-lg">
                    <img src="https://placehold.co/400x300/3B82F6/ffffff?text=DRUM+SET" alt="Drums (ドラム)の画像" class="w-full h-48 object-cover rounded-lg mb-4">
                    <h4 class="text-2xl font-bold text-gray-900 mb-4">Drums (ドラム)</h4>
                    <!-- 説明文 --><p class="text-gray-600">太鼓展の主役！バスドラム、スネアドラム、タムなど複数の太鼓とシンバルを組み合わせたセット。叩き方の基本を教えます。</p>
                </div>
                <!-- Conga (コンガ) --><div class="drum-card p-6 rounded-xl shadow-lg">
                    <img src="https://placehold.co/400x300/34D399/ffffff?text=CONGA" alt="Conga (コンガ)の画像" class="w-full h-48 object-cover rounded-lg mb-4">
                    <h4 class="text-2xl font-bold text-gray-900 mb-4">Conga (コンガ)</h4>
                    <!-- 説明文 --><p class="text-gray-600">キューバ発祥の細長い太鼓。手で叩いて、高音から低音まで様々なリズムを生み出します。ラテンのリズムに挑戦！</p>
                </div>
                <!-- Djembe (ジャンベ) --><div class="drum-card p-6 rounded-xl shadow-lg">
                    <img src="https://placehold.co/400x300/FBBF24/ffffff?text=DJEMBE" alt="Djembe (ジャンベ)の画像" class="w-full h-48 object-cover rounded-lg mb-4">
                    <h4 class="text-2xl font-bold text-gray-900 mb-4">Djembe (ジャンベ)</h4>
                    <!-- 説明文 --><p class="text-gray-600">西アフリカで生まれたゴブレット型（高坏型）の太鼓。芯のある深い低音と、鋭い高音が魅力です。</p>
                </div>
                <!-- Bongo (ボンゴ) --><div class="drum-card p-6 rounded-xl shadow-lg">
                    <img src="https://placehold.co/400x300/EF4444/ffffff?text=BONGO" alt="Bongo (ボンゴ)の画像" class="w-full h-48 object-cover rounded-lg mb-4">
                    <h4 class="text-2xl font-bold text-gray-900 mb-4">Bongo (ボンゴ)</h4>
                    <!-- 説明文 --><p class="text-gray-600">大小2つ一組の太鼓。コンガより軽やかで明るい音色です。座って膝に挟んで叩くスタイルが特徴です。</p>
                </div>
                <!-- Snare drum (スネアドラム) --><div class="drum-card p-6 rounded-xl shadow-lg">
                    <img src="https://placehold.co/400x300/8B5CF6/ffffff?text=SNARE+DRUM" alt="Snare drum (スネアドラム)の画像" class="w-full h-48 object-cover rounded-lg mb-4">
                    <h4 class="text-2xl font-bold text-gray-900 mb-4">Snare drum (スネアドラム)</h4>
                    <!-- 説明文 --><p class="text-gray-600">ドラムセットの要。裏側にあるスナッピー（響き線）による「ジャッ」という歯切れの良い音が特徴です。</p>
                </div>
                <!-- 締太鼓 (しめだいこ) --><div class="drum-card p-6 rounded-xl shadow-lg">
                    <img src="https://placehold.co/400x300/EC4899/ffffff?text=SHIME+DAIKO" alt="締太鼓 (しめだいこ)の画像" class="w-full h-48 object-cover rounded-lg mb-4">
                    <h4 class="text-2xl font-bold text-gray-900 mb-4">締太鼓 (しめだいこ)</h4>
                    <!-- 説明文 --><p class="text-gray-600">日本の和太鼓の一つ。高い音域を持ち、祭囃子などで活躍します。バチを使った叩き方を体験できます。</p>
                </div>

                <!-- Bass Drum (バスドラム) --><div class="drum-card p-6 rounded-xl shadow-lg">
                    <img src="https://placehold.co/400x300/10B981/ffffff?text=BASS+DRUM" alt="Bass Drum (バスドラム)の画像" class="w-full h-48 object-cover rounded-lg mb-4">
                    <h4 class="text-2xl font-bold text-gray-900 mb-4">Bass Drum (バスドラム)</h4>
                    <!-- 説明文 --><p class="text-gray-600">吹奏楽やオーケストラで使われる、非常に大きな太鼓。低く力強い音が特徴で、曲の土台となる役割を果たします。マーチング用とスタンドタイプを展示予定です。</p>
                </div>
                <!-- 長胴太鼓 (ながどうだいこ) --><div class="drum-card p-6 rounded-xl shadow-lg">
                    <img src="https://placehold.co/400x300/F97316/ffffff?text=NAGADO+DAIKO" alt="長胴太鼓 (ながどうだいこ)の画像" class="w-full h-48 object-cover rounded-lg mb-4">
                    <h4 class="text-2xl font-bold text-gray-900 mb-4">長胴太鼓 (ながどうだいこ)</h4>
                    <!-- 説明文 --><p class="text-gray-600">日本の伝統的な太鼓の代表格。一本の木をくり抜いて作られ、深く響く音が特徴です。「太鼓体験」の主役として、その迫力を実感できます。</p>
                </div>
                
            </div>
            
            <p class="text-center text-lg text-gray-700 mt-12">※展示内容は変更になる場合があります。その他、小物打楽器（タンバリン、トライアングルなど）も体験できます！</p>
        </div>
    </section>

    <!-- 開催概要セクション --><section id="details" class="py-16 md:py-24 bg-white">
        <div class="max-w-xl mx-auto px-4 text-center">
            <h3 class="text-3xl font-bold text-gray-900 mb-12 border-b-4 border-primary inline-block pb-1">開催概要</h3>
            
            <div class="space-y-6 text-left p-8 rounded-xl shadow-xl border-t-8 border-secondary bg-gray-50">
                <div class="flex items-center border-b pb-3">
                    <p class="font-bold text-xl w-32 flex-shrink-0">タイトル</p>
                    <p class="text-xl font-extrabold text-primary ml-4">見て・聴いて・叩いて楽しむ太鼓展！</p>
                </div>
                <div class="flex items-center border-b pb-3">
                    <p class="font-bold text-xl w-32 flex-shrink-0">日　時</p>
                    <p class="text-xl ml-4">**11月11日** (土) 10:00 〜 16:00 (予定)</p>
                </div>
                <div class="flex items-center border-b pb-3">
                    <p class="font-bold text-xl w-32 flex-shrink-0">場　所</p>
                    <p class="text-xl ml-4">**浜田高校 吹奏楽部室**</p>
                </div>
                <div class="flex items-center border-b pb-3">
                    <p class="font-bold text-xl w-32 flex-shrink-0">入場料</p>
                    <p class="text-3xl font-extrabold text-red-600 ml-4">無料</p>
                </div>
                <div class="pt-4">
                    <p class="font-bold text-lg mb-2">主　催</p>
                    <p class="text-gray-700">太鼓推進委員会</p>
                </div>
            </div>
            
            <!-- QRコード関連のブロックは削除されました。 -->

            <div class="flex flex-col sm:flex-row justify-center space-y-4 sm:space-y-0 sm:space-x-4 mt-10">
                <button onclick="showContactMessage()" class="bg-primary text-white py-3 px-8 rounded-full text-lg font-bold hover:bg-red-700 transition duration-300 shadow-lg">
                    お問い合わせ
                </button>
                <!-- 申し込みボタン (詳細) --><a href="https://docs.google.com/forms/d/e/1FAIpQLScPoAQWz6z7tLgch5pKRH5t3tkQE9VNBxU-seAffpTDkH9CKA/viewform?usp=header" target="_blank" class="bg-secondary text-dark-bg py-3 px-8 rounded-full text-lg font-bold hover:bg-yellow-400 transition duration-300 shadow-lg inline-block">
                    太鼓展に申し込む
                </a>
            </div>
            <p id="contact-message" class="mt-4 text-sm text-gray-600 hidden">
                <!-- 問い合わせメッセージ表示エリア --></p>
        </div>
    </section>

    <!-- アクセスセクション --><section id="access" class="py-16 md:py-24 bg-gray-100">
        <div class="max-w-4xl mx-auto px-4">
            <h3 class="text-3xl font-bold text-center text-gray-900 mb-12 border-b-4 border-primary inline-block pb-1">アクセス</h3>
            
            <div class="bg-white p-8 rounded-xl shadow-lg">
                <p class="text-xl font-bold mb-4">会場：島根県立浜田高等学校 吹奏楽部室</p>
                
                <!-- Google Map埋め込み --><div class="mb-6 h-64 rounded-xl overflow-hidden shadow-lg">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3238.2520864353457!2d132.0950074755146!3d34.89967779778235!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x355a599558f37457%3A0x39ad786ee39620af!2z5b6D6Z2S6auY5L2J5qyn5bee5biC!5e0!3m2!1sja!2sjp!4v1700000000000!5m2!1sja!2sjp" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>

                <h4 class="text-2xl font-semibold text-primary mb-3">交通案内</h4>
                <ul class="list-disc list-inside space-y-2 text-gray-700 ml-4">
                    <!-- 徒歩時間を14分に修正済み -->
                    <li>JR山陰本線「浜田駅」より徒歩約14分。</li>
                    <li>石見交通バス「県立大学前」下車、徒歩約5分。</li>
                    <!-- 駐車場の案内 --><li>**【お車でお越しの方へ】** 当日は高校の駐車場をご利用いただけます。案内に従って駐車してください。</li>
                    <li>**【重要】** 部室への立ち入りは、当日の案内係の指示に従ってください。</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- フッター --><footer class="bg-dark-bg text-white py-8">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <p class="text-lg font-bold mb-2">太鼓推進委員会</p>
            <p>&copy; 2024 Taiko Promotion Committee. All rights reserved.</p>
        </div>
    </footer>

</body>
</html>
