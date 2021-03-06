---
title: "Symantec、GeoTrust、RapidSSL、Thawte、Verisign 証明書への信頼が 2018 年 10 月にすべて失われます"
date: "2018-06-05T12:53:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["63"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1460062"
      title: "Bug 1460062 - Enforce Symantec distrust in Firefox 63"
    - url: "https://blog.mozilla.org/security/2018/03/12/distrust-symantec-tls-certificates/"
      title: "Mozilla Security Blog: Distrust of Symantec TLS Certificates"
---
[様々な認証局運用問題](https://wiki.mozilla.org/CA:Symantec_Issues) に起因する、複数ベンダーによる Symantec に対する信頼無効化措置の最終段階として、10 月 16 日公開の Firefox 63 と 10 月 23 日公開の [Google Chrome 70](https://security.googleblog.com/2017/09/chromes-plan-to-distrust-symantec.html) は、Symantec から発行されたすべての既存 TLS サーバー証明書への信頼を取り消します。これには、GeoTrust、RapidSSL、Thawte、Verisign ブランド傘下で発行されたものも含まれます。

[Firefox 58](https://www.fxsitecompat.com/ja/docs/2018/symantec-issued-certificates-will-soon-be-distrusted/) 以降、影響を受ける証明書に対してコンソール警告が表示されており、[Firefox 60](https://www.fxsitecompat.com/ja/docs/2018/symantec-certificates-issued-before-june-2016-are-now-distrusted/) では 2016 年 6 月より前に発行された証明書への信頼が既に失われています。Firefox 63 以降、発行日に関わらず、Symantec から発行された証明書を使ったサイトに対して「安全でない接続」のエラーページが表示されます。

望まないエラーページを避けるため、それらのいずれかの証明書を使っているウェブマスターの皆さんは、できる限り早く [それを新しいものと交換する](https://www.symantec.com/connect/ja/blogs/symantec-ssltls) か、他の認証局から代わりの証明書を入手しなくてはなりません。私たちは、信頼できる証明書を無償で提供している [Let's Encrypt](https://letsencrypt.org/) を推奨します。
