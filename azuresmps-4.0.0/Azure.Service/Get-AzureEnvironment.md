---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106352"
---
# Get-AzureEnvironment

## SYNOPSIS
Azure ortamlarını alır

## INDEKI

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureEnvironment** cmdlet 'ı Windows PowerShell 'In kullanabildiği Azure ortamlarını alır.

Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.
Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.
Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

**Get-AzureEnvironment** cmdlet 'i Azure 'dan değil, abonelik veri dosyanızdaki ortamları alır.
Abonelik verileri dosyası güncel değilse, bunu yenilemek için **Add-AzureAccount** veya **Import-publishsettingsfile** cmdlet 'ini çalıştırın.

Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

## ÖRNEKLERDEN

### Örnek 1: tüm ortamları alma
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

Bu komut Windows PowerShell 'in kullanabildiği tüm ortamları alır.

### Örnek 2: ada göre ortam alma
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

Bu örnekte, Azurecyüksek ortamı alınır.

### Örnek 3: tüm ortamlardaki tüm özellikleri alma
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

Bu komut, tüm ortamların tüm özelliklerini alır.

Komut **Get-AzureEnvironment** cmdlet 'ini kullanarak bu hesabın tüm Azure ortamlarını alır.
Ardından, her ortamdaki **Name** parametresiyle **Get-AzureEnvironment** komutunu çalıştırmak için **ForEach-Object** cmdlet 'ini kullanır.
**Name** parametresinin değeri, her ortamın **environmentname** özelliğidir.

Parametresiz, **Get-AzureEnvironment** , bir ortamın yalnızca seçili özelliklerini alır.

## PARAMETRELERINE

### -Ad
Yalnızca belirtilen ortamı alır.
Ortam adını yazın.
Parametre değeri büyük/küçük harfe duyarlıdır.
Joker karakterler kullanılamaz.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.

## ÇıKıŞLAR

### System. Management. Automation. PSCustomObject
Varsayılan olarak **Get-AzureEnvironment** , özel bir nesne döndürür.

### Microsoft. Windowsazme. Commands. Utilities. Common. WindowsAzureEnvironment
**Name** parametresiyle **Get-AzureEnvironment** 'ı çalıştırdığınızda, bir **windowsazureenvironment** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-Azuikinci dosyayı](./Get-AzurePublishSettingsFile.md)

[Import-Azuyeniden yayımlayan ayarları dosyası](./Import-AzurePublishSettingsFile.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


