---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106261"
---
# Import-AzurePublishSettingsFile

## SYNOPSIS
Windows PowerShell 'de Azure hesaplarınızı yönetmenizi sağlayan bir yayımlama ayarları dosyası içeri aktarır.

## INDEKI

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Import-Azuikinci yeniden yükleyen Settingsfıle** cmdlet 'ı, Azure hesaplarınız hakkında bilgi içeren bir yayımlama ayarları dosyası (*. publishsettings) içeri aktarır ve bilgisayarınıza bir abonelik verileri dosyası kaydeder.
Cmdlet tamamlandığında, Azure hesaplarınızı Windows PowerShell 'de yönetebilirsiniz.

**İmport-Azuikinci** kayıt ayarları dosyasını çalıştırmadan önce, yayınlama ayarları dosyasını indiren ve kaydeden **Get-Azu**

Azure hesabınızı Windows PowerShell 'in kullanımına sunmak için, bir yayımlama ayarları dosyası veya **Add-AzureAccount** cmdlet 'ini kullanabilirsiniz.
Yayımlama ayarları dosyaları oturumu önceden hazırlamanıza olanak tanır; böylece komut dosyalarını ve arka plan işlerini katılımsız olarak çalıştırabilirsiniz.
Ancak, tüm hizmetler yayımlama ayarları dosyalarını desteklemez.
Örneğin, **AzureResourceManager** modülü yayımlama ayarları dosyalarını desteklemez.

**Güvenlik notu:** Yayımlama ayarları dosyaları kodlanmış ancak şifrelenmemiş bir yönetim sertifikası içerir.
Kötü niyetli kullanıcılar yayımlama ayarları dosyanıza erişlerse, Azure hizmetlerini düzenleyebilir, oluşturabilir ve silebilir.
En iyi güvenlik uygulaması olarak, dosyayı Indirmeler veya belgeler klasörünüzdeki bir konuma kaydedin ve sonra da ayarları içeri aktarmak için **import-azudandanayardandosya** cmdlet 'ini kullandıktan sonra silin.

## ÖRNEKLERDEN

### Örnek 1: dosya Içeri aktarma
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

Bu komut, "C:\Temp\MyAccount.publishsettings" dosyasını içeri aktarır.

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

### -PublishSettingsFile
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### Yabilirsiniz
Bu cmdlet hiçbir çıkış üretmez.

## NOTLARıNDA
* "Yayımlama ayarları dosyası". publishsettings dosya adı uzantısına sahip bir XML dosyasıdır. Dosya, Azure abonelikleriniz için yönetim kimlik bilgilerini sağlayan kodlanmış bir sertifika içeriyor. Bu dosyayı içeri aktardıktan sonra güvenlik risklerini engellemek için dosyayı silin.
* "Abonelik verileri dosyası", bilgisayarınıza güvenle kaydedibir XML dosyasıdır. Varsayılan olarak, gezici kullanıcı profilinize ($home/AppData/Roaming) kaydedilir.

## ILGILI BAĞLANTıLAR

[Azure PowerShell 'i yükleme ve yapılandırma](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-Azuikinci dosyayı](./Get-AzurePublishSettingsFile.md)


