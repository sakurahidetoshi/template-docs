# BASE Templateドキュメント
BASE Templateのドキュメントです。BASE Templateを使うにはHTML、CSS、JavaScriptの基本的な知識が必須です。事前に学習をお願いします。

## はじめに
BASE Templateとは、BASEのショップのテンプレートを編集できる機能のことです。テンプレートを自由に編集して、自分のオリジナルのテーマを作ることができます。デザインオプションを独自に設定することもできます。

## 利用開始
1. テンプレート編集Appsをインストール。
2. メニューのデザイン編集をクリック。
3. HTMLを編集するをクリック。

BASE Templateはテンプレート変数を使って編集します。テンプレート変数には、変数とブロックの2種類があります。使い方はBASEのデフォルトテーマを参考にしてみてください。

*変数の例)*

```
<html>
	<head>
		...
	</head>
	<body>
		<h1><a href="{IndexPageURL}">{LogoTag}</a></h1>
	</body>
</html>
```

*ブロックの例)*

```
<html>
	<head>
		...
	</head>
	<body>
		<ul>
			{block:Items}
			<li>...</li>
			{/block:Items}
		</ul>
	</body>
</html>
```

## テンプレート変数の説明

### ループ

| タグ名 | 説明 |
|--------|------|
| {block:Items} | 商品のループ |
| {block:AppsItemCategoryCategories} | 商品カテゴリーのループ (カテゴリーAppsのインストールが必要) |

### if 非表示

| タグ名 | 説明 |
|--------|------|
| {block:Hidden} | このブロックで囲むと何も表示されない |

### if イテレータ

| タグ名 | 説明 |
|--------|------|
| {block:Item[1-24]} | 商品が何番目のループ `例) {block:Item2}2番目{/block:Item2}` |
| {block:NotItem[1-24]} | 商品が何番目のループではない `例) {block:NotItem3}3番目ではない{/block:NotItem3}` |
| {block:Odd} | 商品が奇数番目のループ |
| {block:Even} | 商品が偶数番目のループ |

### if ページ

| タグ名 | 説明 |
|--------|------|
| {block:IndexPage} | トップページ |
| {block:ItemPage} | 商品ページ |
| {block:AboutPage} | aboutページ |
| {block:ContactPage} | contactページ |
| {block:PrivacyPage} | プライバシーポリシーページ |
| {block:LawPage} | 特商法ページ |
| {block:BlogPage} | blogページ |
| {block:NotIndexPage} | トップページではない |
| {block:NotItemPage} | 商品ページではない |
| {block:NotAboutPage} | aboutページではない |
| {block:NotContactPage} | contactページではない |
| {block:NotPrivacyPage} | プライバシーポリシーページではない |
| {block:NotLawPage} | 特商法ページではない |
| {block:NotBlogPage} | blogページではない |
| {block:LoadItemsPage} | 商品ロードページ |
| {block:NotLoadItemsPage} | 商品ロードページではない |

### if ショップ

| タグ名 | 説明 |
|--------|------|
| {block:ShopTwitterId} | Twitter IDがある |
| {block:ShopFacebookId} | Facebook IDがある |
| {block:ShopAmebaId} | Ameba IDがある |
| {block:ShopInstagramId} | Instagram IDがある |
| {block:NoShopTwitterId} | Twitter IDがない |
| {block:NoShopFacebookId} | Facebook IDがない |
| {block:NoShopAmebaId} | Ameba IDがない |
| {block:NoShopInstagramId} | Instagram IDがない |
| {block:ShopPublic} | ショップが公開されている |
| {block:NotShopPublic} | ショップが公開されていない |

### if デザインオプション

| タグ名 | 説明 |
|--------|------|
| {block:NavColor} | ナビゲーションカラーが設定されている |
| {block:TextColor} | テキストカラーが設定されている |
| {block:LinkColor} | リンクカラーが設定されている |

### if 商品

| タグ名 | 説明 |
|--------|------|
| {block:HasItems} | 商品がある |
| {block:NoItems} | 商品がない |
| {block:HasItemStock} | 商品の在庫がある |
| {block:NoItemStock} | 商品の在庫がない |
| {block:ItemDigitalContent} | デジタルコンテンツの商品 (デジタルコンテンツAppsのインストールが必要) |
| {block:ItemImage1} | 商品画像1がある |
| {block:ItemImage2} | 商品画像2がある |
| {block:ItemImage3} | 商品画像3がある |
| {block:ItemImage4} | 商品画像4がある |
| {block:ItemImage5} | 商品画像5がある |
| {block:NoItemImage1} | 商品画像1がない |
| {block:NoItemImage2} | 商品画像2がない |
| {block:NoItemImage3} | 商品画像3がない |
| {block:NoItemImage4} | 商品画像4がない |
| {block:NoItemImage5} | 商品画像5がない |

### if Apps

| タグ名 | 説明 |
|--------|------|
| {block:AppsItemCategory} | カテゴリーAppsをインストールしている |
| {block:AppsBlog} | Blog Appsをインストールしている |
| {block:AppsI18n} | 海外対応Appsをインストールしている |
| {block:AppsDownload} | デジタルコンテンツAppsをインストールしている |
| {block:AppsItemLabel} | ラベルAppsをインストールしている |

### BASE

| タグ名 | 説明 |
|--------|------|
| {BASEURL} | BASEのURL `https://thebase.in` |
| {BASEDomain} | BASEのドメイン `thebase.in` |

### ページ

| タグ名 | 説明 |
|--------|------|
| {IndexPageURL} | トップページのURL |
| {ItemPageURL} | 商品ページのURL |
| {AboutPageURL} | aboutページのURL |
| {BlogPageURL} | blogページのURL |
| {ContactPageURL} | contactページのURL |
| {PrivacyPageURL} | プライバシーポリシーページのURL |
| {LawPageURL} | 特商法ページのURL |
| {LoadItemsPageURL} | 商品ロードページのURL。ページングのajaxで使用する。 `例) url: "{LoadItemsPageURL}" + next_page + "{LoadItemsPageURLParams}",` |
| {LoadItemsPageURLParams} | 商品ロードページのURLのパラメーター。ページングのajaxで使用する。 `例) url: "{LoadItemsPageURL}" + next_page + "{LoadItemsPageURLParams}",` |

### HTMLヘッダー

| タグ名 | 説明 |
|--------|------|
| {PageTitle} | ページのタイトル |
| {HeadLinkNextPrevTag} | クローラー向けの前のページ、次のページのリンクです。 `例) <head>... {block:IndexPage}{HeadLinkNextPrevTag}{/block:IndexPage} ...</head>` |
| {MetaItemInfoTag} | 商品のメタ情報 `例) <head>... {block:ItemPage}{MetaItemInfoTag}{/block:ItemPage} ...</head>` |
| {MetaShopInfoTag} | ショップのメタ情報 `例) <head>... {block:NotItemPage}{MetaShopInfoTag}{/block:NotItemPage} ...</head>` |
| {GoogleAnalyticsTag} | *[必須]* Google Analyticsのタグ。Google Analytics Appsで設定したタグがここに表示されます。自分で直接Google Analyticsタグを貼らないでください。 |

### テンプレート

| タグ名 | 説明 |
|--------|------|
| {Counter} | 表示されるごとに1から順に数字が表示される特殊な変数です |
| {MaxPageNumber} | 最大ページ数。ページングのajaxで使用する。 |
| {NextPageNumber} | 次のページ。ページングのajaxで使用する。 |
| {IllegalReportMessageTag} | 「違反通報ありがとうございます」のメッセージ。セッションを使って表示しているのでthebase.inドメインのショップでしか表示されません。 |
| {ItemSelectTag} | 商品ページのselectのタグ |
| {EmbedWidgetTag} | 商品ページの外部サイトに貼るのタグ |
| {BASEMenuTag} | *[必須]* BASEのトップとカートのリンクのタグ |
| {ContactContentsTag} | *[必須]* contactページのコンテンツのタグ |
| {PrivacyContentsTag} | *[必須]* プライバシーポリシーページのコンテンツのタグ |
| {LawContentsTag} | *[必須]* 特商法ページのコンテンツのタグ |
| {BlogContentsTag} | blogページのコンテンツのタグ |
| {ItemAttentionTag} | *[必須]* 商品ページの注意文のタグ |
| {IllegalReportTag} | *[必須]* 商品ページの通報するのタグ |

### ショップ

| タグ名 | 説明 |
|--------|------|
| {ShopId} | ショップのID |
| {ShopDomain} | ショップのドメイン `例) shop.thebase.in` |
| {ShopURL} | ショップのURL `例) http://shop.thebase.in` |
| {ShopName} | ショップの名前 |
| {ShopIntroduction} | ショップの説明 |
| {ShopTwitterId} | ショップのTwitter ID |
| {ShopFacebookId} | ショップのFacebook ID |
| {ShopAmebaId} | ショップのAmeba ID |
| {ShopInstagramId} | ショップのInstagram ID |

### デザインオプション

| タグ名 | 説明 |
|--------|------|
| {NavColor} | ナビゲーションのカラー |
| {TextColor} | テキストのカラー |
| {LinkColor} | リンクのカラー |
| {LogoTag} | *[必須]* ロゴのタグ |
| {BackgroundTag} | *[必須]* バックグラウンドのタグ |

### 商品

| タグ名 | 説明 |
|--------|------|
| {ItemId} | 商品のID |
| {ItemTitle} | 商品の名前 |
| {ItemPrice} | 商品の価格 |
| {ItemStock} | 商品の在庫数 |
| {ItemDetail} | 商品の説明 (改行がbrタグになっている) |
| {ItemDetailNoBr} | 商品の説明 (改行がbrタグになっていない) |
| {ItemDigitalContent} | 商品のデジタルコンテンツのファイル名 (デジタルコンテンツAppsのインストールが必要) |
| {ItemImage[1-5]URL-origin} | 商品画像のオリジナルサイズ `例) <img src="{ItemImage2URL-origin}">` |
| {ItemImage[1-5]URL-76} | 商品画像の76pxサイズ。ない場合は近いサイズ。 |
| {ItemImage[1-5]URL-146} | 商品画像の146pxサイズ。ない場合は近いサイズ。 |
| {ItemImage[1-5]URL-300} | 商品画像の300pxサイズ。ない場合は近いサイズ。 |
| {ItemImage[1-5]URL-500} | 商品画像の500pxサイズ。ない場合は近いサイズ。 |
| {ItemImage[1-5]URL-640} | 商品画像の640pxサイズ。ない場合は近いサイズ。 |
| {ItemNoImageURL} | no imageの画像 |

### Apps

| タグ名 | 説明 |
|--------|------|
| {AppsItemCategoryTag} | 商品カテゴリーのタグ (カテゴリーAppsのインストールが必要) |
| {AppsI18nTag} | 言語切替のタグ (海外対応Appsのインストールが必要) |
| {AppsItemLabelTag} | 商品ラベルのタグ (ラベルAppsのインストールが必要) |
| {AppsItemCategoryCategoryName} | 商品カテゴリーの名前 (カテゴリーAppsのインストールが必要) `例) {block:AppsItemCategoryCategories}{AppsItemCategoryCategoryName}{/block:AppsItemCategoryCategories}` |
| {AppsItemCategoryCategoryCount} | 商品カテゴリーの商品数 (カテゴリーAppsのインストールが必要) `例) {block:AppsItemCategoryCategories}{AppsItemCategoryCategoryName} ({AppsItemCategoryCategoryCount}){/block:AppsItemCategoryCategories}` |
| {AppsItemCategoryCategoryPageURL} | 商品カテゴリーのページのURL (カテゴリーAppsのインストールが必要) `例) {block:AppsItemCategoryCategories}<a href="{AppsItemCategoryCategoryPageURL}">{AppsItemCategoryCategoryName}</a>{/block:AppsItemCategoryCategories}` |

### ローカライズテキスト

| タグ名 | 説明 |
|--------|------|
| {lang:Privacy} | プライバシーポリシー |
| {lang:Law} | 特定商取引法に基づく表記 |
| {lang:AddToCart} | カートに入れる |
| {lang:NoItemsMessage} | 出品されている商品がありません。 |
| {lang:NotShopPublicMessage} | [ショップ名]は、現在準備中です。 |
| {lang:SeeDetails} | 詳細を見る |
| {lang:Tweet} | ツイート |

## デザインオプションの独自設定


