---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
gitcommit: https://github.com/Azure/azure-powershell/blob/89262bc4144696c69376c3fb654c881de55b6450
ms.openlocfilehash: 2e9d3689a29a54f7af873cd1a11fdbc343509eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765079"
---
# New-AzureStorageContext

## SYNOPSIS
Azure depolama bağlamı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### AccountNameAndKey (varsayılan)
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### ConnectionString
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## Tanım
**New-AzureStorageContext** cmdlet 'ı Azure depolama bağlamı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: depolama hesabı adı ve anahtarı belirterek bağlam oluşturma
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Bu komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.

### Örnek 2: bağlantı dizesi belirterek bağlam oluşturma
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Bu komut, ContosoGeneral hesabı için belirtilen bağlantı dizesine dayalı bir bağlam oluşturur.

### Örnek 3: anonim depolama hesabı için bağlam oluşturma
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Bu komut, ContosoGeneral adlı hesap için anonim kullanım bağlamı oluşturur.
Komut HTTP 'yi bağlantı protokolü olarak belirtir.

### Örnek 4: yerel geliştirme depolama hesabını kullanarak bağlam oluşturma
```
C:\PS>New-AzureStorageContext -Local
```

Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur.
Komut *Yerel* parametreyi belirtir.

### Örnek 5: yerel geliştirici depolama hesabı kapsayıcısını alma
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

Bu komut, yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve ardından ardışık düzen işlecini kullanarak yeni bağlamı **Get-AzureStorageContainer** cmdlet 'ine geçirir.
Komut, yerel geliştirici depolama hesabı için Azure depolama kapsayıcısını alır.

### Örnek 6: birden çok kapsayıcı alma
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

İlk komut yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturur ve bu $Context bağlamı 01 değişkenine depolar.

İkinci komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur ve bu bağlamı $Context 02 değişkeninde depolar.

Son komutu, **Get-AzureStorageContainer** kullanarak $Context 01 ve $Context 02 ' da depolanan bağlamların kapsayıcılarını alır.

### Örnek 7: uç noktayla bağlam oluşturma
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Bu komut, belirtilen depolama uç noktasına sahip bir Azure depolama bağlamı oluşturur.
Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.

### Örnek 8: belirtilen ortamla bağlam oluşturma
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Bu komut, belirtilen Azure ortamına sahip bir Azure depolama bağlamı oluşturur.
Komut, ContosoGeneral adlı hesap için belirtilen anahtarı kullanan bir bağlam oluşturur.

### Örnek 9: SAS belirteci kullanarak bağlam oluşturma
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

İlk komut, ContosoMain adlı kapsayıcı için **New-AzureStorageContainerSASToken** cmdlet 'INI kullanarak SAS belirteci oluşturur ve bu belirteci $SasToken değişkeninde depolar.
Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.

İkinci komut, $SasToken depolanan SAS belirtecini kullanan ContosoGeneral adlı hesap için bir bağlam oluşturur ve bu bağlamı $Context değişkeninde depolar.

Son komutu, $Context 'da depolanan bağlamı kullanarak ContosoMain adlı kapsayıcıyla ilişkili tüm blob 'ları listeler.

## PARAMETRELERINE

### -Anonim
Bu cmdlet 'in anonim oturum açma için bir Azure depolama bağlamını oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Azure depolama bağlamı için bir bağlantı dizesi belirtir.

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Uç nokta
Azure depolama bağlamının uç noktasını belirtir.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ortam
Azure ortamını belirtir.
Bu parametre için kabul edilebilir değerler: Azurecyüksek ve AzureChinaCloud.
Daha fazla bilgi için yazın `Get-Help Get-AzureEnvironment` .

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yerel
Bu cmdlet 'in yerel geliştirme depolama hesabını kullanarak bir bağlam oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -İletişim kuralı
Aktarma Protokolü (https/http).

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Bağlam için paylaşılan bir erişim Imzası (SAS) belirteci belirtir.

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Bir Azure depolama hesabı anahtarı belirtir.
Bu cmdlet, bu parametrenin belirttiği anahtar için bağlam oluşturur.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Azure depolama hesap adını belirtir.
Bu cmdlet, bu parametrenin belirttiği hesap için bağlam oluşturur.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### AzureStorageContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)


