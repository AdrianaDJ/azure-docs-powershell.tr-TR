---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105950"
---
# Set-AzureSubscription

## SYNOPSIS
Azure aboneliğini değiştirir.

## INDEKI

### Updatesubscriptionbyıdparametersetname (varsayılan)
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UpdateSubscriptionByNameParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AddSubscriptionParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Set-azuyeniden gönderme Betikleşme** , bir Azure abonelik nesnesinin özelliklerini oluşturur ve değiştirir.
Varsayılan aboneliğiniz olmayan bir Azure aboneliğiyle çalışmak veya geçerli depolama hesabınızı değiştirmek için bu cmdlet 'i kullanabilirsiniz.
Geçerli ve varsayılan abonelikler hakkında bilgi için, **Select-Azuyeniden komut Scription** cmdlet 'ine bakın.

Bu cmdlet, gerçek Azure aboneliğinizi değil, bir Azure aboneliği nesnesinde çalışır.
Bir Azure aboneliği oluşturmak ve sağlamak için, [Azure portalını](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .

Bu cmdlet, Windows PowerShell 'e bir Azure hesabı eklemek için **Add-AzureAccount** veya **Import-Azuyeniden yükleyen SettingsFile** cmdlet 'ini kullandığınızda oluşturduğunuz abonelik verileri dosyasındaki verileri değiştirir.

Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

## ÖRNEKLERDEN

### Örnek 1: varolan bir subscription1
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

Bu örnek, ContosoEngineering adlı aboneliğin sertifikasını değiştirir.

### Örnek 2: hizmet uç noktasını değiştirme
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

Bu komut, ContosoEngineering aboneliği için özel bir hizmet uç noktası ekler veya değiştirir.

### Örnek 3: özellik değerlerini Temizleme
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

Bu komut, sertifika ve ResourceManagerEndpoint özelliklerinin değerlerini null ($Null) olarak ayarlar.
Bu, diğer ayarları değiştirmeden bu özelliklerin değerlerini temizler.

### Örnek 4: alternatif bir abonelik veri dosyası kullanın
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

Bu komut ContosoFinance aboneliğinin geçerli depolama hesabını ContosoStorage01 olarak değiştirir.
Komut, C:\Azure\SubscriptionData.xml aboneliği veri dosyasındaki verileri değiştirmek için **subscriptionveri** dosyası parametresini kullanır.
Varsayılan olarak **set-Azuyeniden gönderme betikte** , gezici kullanıcı profilinizde varsayılan abonelik verileri dosyası kullanılır.

## PARAMETRELERINE

### -Sertifika
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CurrentStorageAccountName
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

### -ResourceManagerEndpoint
Hesap ile ilişkili kaynak gruplarıyla ilgili veriler de içinde olmak üzere, Azure Resource Manager verilerinin uç noktasını belirtir.
Azure Resource Manager hakkında daha fazla bilgi için [Azure Resource Manager cmdlet 'lerinin](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) ve [Kaynak Yöneticisi ile Windows PowerShell](https://go.microsoft.com/fwlink/?LinkID=394767)  'in ( https://go.microsoft.com/fwlink/?LinkID=394767) .

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

### -ServiceEndpoint
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

### -SubscriptionID
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
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

### None veya System. Boolean
*Passin* parametresini kullandığınızda, bu cmdlet bir Boole değeri döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-Azuyeniden gönderme](./Get-AzureSubscription.md)

[Import-Azuyeniden yayımlayan ayarları dosyası](./Import-AzurePublishSettingsFile.md)

[Remove-Azuyeniden gönderiliyor](./Remove-AzureSubscription.md)

[Select-Azuyeniden gönderme](./Select-AzureSubscription.md)


