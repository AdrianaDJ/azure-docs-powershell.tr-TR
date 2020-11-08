---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105633"
---
# Get-AzurePublishSettingsFile

## SYNOPSIS
Azure aboneliği için yayımlama ayarları dosyasını indirir.

## INDEKI

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-Azuikinci dosyayı** ayarlar cmdlet 'i, hesabınızdaki bir aboneliğin yayımlama ayarları dosyasını indirir.
Komut tamamlandığında, dosyadaki ayarların Windows PowerShell tarafından kullanılabilmesini sağlamak için **Import-PublishSettingsFile** cmdlet 'ini kullanabilirsiniz.

Azure hesabınızı Windows PowerShell 'in kullanımına sunmak için, bir yayımlama ayarları dosyası veya **Add-AzureAccount** cmdlet 'ini kullanabilirsiniz.
Yayımlama ayarları dosyaları oturumu önceden hazırlamanıza olanak tanır; böylece komut dosyalarını ve arka plan işlerini katılımsız olarak çalıştırabilirsiniz.
Ancak, tüm hizmetler yayımlama ayarları dosyalarını desteklemez.
Örneğin, **AzureResourceManager** modülü yayımlama ayarları dosyalarını desteklemez.

**Get-azuyeniden yayımlamadan önce Settings dosyasını** çalıştırdığınızda, varsayılan tarayıcınızı açar ve Azure hesabınızda oturum açmanızı ister ve yayımlama ayarları dosyası için bir dosya sistemi konumu seçin.
Ardından, aboneliğiniz için yayımlama ayarları dosyasını seçtiğiniz dosyaya yükler.

"Yayımlama ayarları dosyası". publishsettings dosya adı uzantısına sahip bir XML dosyasıdır.
Dosya, Azure abonelikleriniz için yönetim kimlik bilgilerini sağlayan kodlanmış bir sertifika içeriyor.

**Güvenlik notu:** Yayımlama ayarları dosyaları, Azure aboneliğinizi ve hizmetlerinizi yönetmek için kullanılan kimlik bilgilerini içerir.
Kötü niyetli kullanıcılar yayımlama ayarları dosyanıza erişlerse, Azure hizmetlerini düzenleyebilir, oluşturabilir ve silebilir.
En iyi güvenlik uygulaması olarak, dosyayı Indirmeler veya belgeler klasörünüzdeki bir konuma kaydedin ve sonra da ayarları içeri aktarmak için **import-azudandanayardandosya** cmdlet 'ini kullandıktan sonra silin.

Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

## ÖRNEKLERDEN

### Örnek 1: yayımlama ayarları dosyasını Indirme
```
PS C:\> Get-AzurePublishSettingsFile
```

Bu komut varsayılan tarayıcınızı açar, Windows Azure hesabınıza bağlanır ve ardından hesabınızın. publishsettings dosyasını indirir.

### Örnek 2: bölge belirtme
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

Bu komut, contoso.com etki alanındaki bir hesabın yayımlama ayarları dosyasını indirir.
Bir Microsoft hesabı yerine bir kuruluş hesabıyla oturum açtığınızda, **bölge** parametresiyle bir komut kullanın.

## PARAMETRELERINE

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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Komut başarılı olduysa $True ve başarısız olursa $False döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Bölge
Kuruluş KIMLIĞINDE kuruluş belirtir.
Örneğin, Azure 'da oturum açarsanız admin@contoso.com , **bölge** parametresinin değeri contoso.com olur.
Azure portalında oturum açmak için kuruluş KIMLIĞI kullandığınızda bu parametreyi kullanın.
Outlook.com veya live.com hesabı gibi bir Microsoft hesabı kullandığınızda bu parametre gerekli değildir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.

## ÇıKıŞLAR

### None veya System. Boolean
*Passin* parametresini kullandığınızda, bu cmdlet bir Boole değeri döndürür.
Aksi halde, bu cmdlet hiçbir çıkış döndürmez

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Import-Azuyeniden yayımlayan ayarları dosyası](./Import-AzurePublishSettingsFile.md)


