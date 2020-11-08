---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106396"
---
# Add-AzureAccount

## SYNOPSIS
Azure hesabını Windows PowerShell 'e ekler.

## INDEKI

### Kullanıcı (varsayılan)
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServicePrincipal
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Add-AzureAccount** cmdlet 'ı, Azure hesabınızın ve aboneliklerinizin Windows PowerShell 'de kullanılabilmesini sağlar.
Windows PowerShell 'de Azure hesabınızda oturum açmak gibidir.
Hesabı oturumu açmak için **Remove-AzureAccount** cmdlet 'ini kullanın.

**Add-AzureAccount** , Azure hesabınızla ilgili bilgileri indirir ve gezici kullanıcı profilinizde bir abonelik verileri dosyasına kaydeder.
Ayrıca, Windows PowerShell 'in sizin adınıza Azure hesabınıza erişmesini sağlayan bir erişim simgesi de alır.
Komut tamamlandığında, Azure hesabınızı Windows PowerShell 'de yönetebilirsiniz.

Azure hesabınızı Windows PowerShell 'in kullanımına sunmak için iki farklı yol vardır.
Bir yönetim sertifikası kullanan Azure Active Directory (Azure AD) kimlik doğrulama erişim belirteçlerini veya **Içeri aktarma-Azuikinci ad ayarları dosyasını** kullanan **Add-AzureAccount** cmdlet 'ini kullanabilirsiniz.
Hangi yöntemin kullanılacağı konusunda rehberlik için, [nasıl yapılır: aboneliğinize nasıl bağlanabilirim](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .

**Add-AzureAccount** ' i çalıştırdığınızda, Azure hesabınızda oturum açmanızı isteyen etkileşimli bir pencere görüntülenir.
Bu oturum açma işlemi, erişim belirtecinin süresi dolana kadar geçerlidir.
Süresi dolduğunda, hesabınıza erişmesi gereken cmdlet 'ler **AzureAccount** 'i yeniden çalıştırmanız istenir.

Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

## ÖRNEKLERDEN

### Örnek 1: hesap ekleme
```
PS C:\> Add-AzureAccount
```

Bu komut Windows PowerShell 'e bir Azure hesabı ekler.
Komutu çalıştırdığınızda, hesabın kullanıcı adını ve parolasını istemek için Windows açılır.

### Örnek 2: alternatif bir abonelik veri dosyası kullanın
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

Bu komut, **AzureAccount doğrudan Add-** ' **u, varsayılan** dosya yerine C:\Testing\SDF.xml dosyasındaki hesap verilerini depolamak için kullanır.

## PARAMETRELERINE

### -Credential
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ortam
Bir Azure ortamı belirtir.

Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.
Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.
Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir. Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet 'e giriş kanalı oluşturamazsınız

## ÇıKıŞLAR

### Yabilirsiniz
Bu cmdlet hiçbir çıkış döndürmez.

## NOTLARıNDA
* **Add-AzureAccount** (ve Azure AD doğrulama yöntemi) **Import-azuikinci** site (ve yönetim sertifikası yöntemi) ile önceliklidir. Hesabınızda **AzureAccount eklentisini** bir kez kullanıyorsanız, Azure AD doğrulama yöntemi kullanılır ve yönetim sertifikası yoksayılır. Azure AD belirtecini kaldırmak ve yönetim sertifikası yöntemini geri yüklemek için **Remove-AzureAccount** cmdlet 'ini kullanın. Daha fazla bilgi için şunu yazın: **Get-Help Remove-AzureAccount**.
* "Kimlik bilgilerinizin süresi doldu. Lütfen tekrar oturum açmak için Add-AzureAccount kullanın. " erişim belirtecinizin süresinin dolduğunu ve Windows PowerShell 'in Azure hesabınıza erişemediğini belirtir. Hesabınıza erişimi geri yüklemek için **Add-AzureAccount** ' i yeniden deneyin.
* Azure PowerShell hesabı ve abonelik cmdlet 'leri, verileri Live Azure hesabından değil, abonelik verileri dosyasından alırlar. Windows PowerShell dışında, örneğin Azure yönetim portalı 'nı kullanarak hesabınızı veya aboneliklerinizi değiştirirseniz, abonelik verileri dosyasını yenilemek için **Add-AzureAccount** ' i yeniden çalıştırarak.

## ILGILI BAĞLANTıLAR

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Import-Azuyeniden yayımlayan ayarları dosyası](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


