---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
ms.openlocfilehash: 99dc4097c1b54459e121e87b9a52e3ab38a325f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593349"
---
# New-AzureStorageTableSASToken

## SYNOPSIS
Bir Azure depolama tablosu için SAS belirteci oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SasPolicy
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzureStorageTableSASToken** cmdlet 'ı bir Azure depolama tablosu Için paylaşılan erişim IMZASı (SAS) belirteci oluşturur.

## ÖRNEKLERDEN

### Örnek 1: tablo için tam izinleri olan SAS belirteci oluşturma
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

Bu komut, ContosoResources adlı tablo için tam izinlerle bir SAS belirteci oluşturur.
Bu belirteç okuma, ekleme, güncelleştirme ve silme izinleri içindir.

### Örnek 2: bir bölüm aralığı için SAS belirteci oluşturma
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

Bu komut, ContosoResources adlı tablo için tam izinlerle SAS belirteci oluşturur.
Komut, belirteci *startpartitionkey* ve *endpartitionkey* parametrelerinin belirttiğiniz aralıkla sınırlar.

### Örnek 3: tablo için depolanan bir erişim ilkesine sahip SAS belirteci oluşturma
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

Bu komut, ContosoResources adlı tablo için bir SAS belirteci oluşturur.
Komut, ClientPolicy01 adlı depolanan erişim ilkesini belirtir.

## PARAMETRELERINE

### -Context
Azure depolama bağlamını belirtir.
Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndPartitionKey
Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki bölüm anahtarını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRowKey
Bu cmdlet 'in oluşturduğu belirteç için aralığın sonundaki satır tuşunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
SAS belirtecinin ne zaman dolacağını belirtir.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
Bu cmdlet 'in SAS belirtecine sahip tam sıra URI olduğunu gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipadressorrange
168.1.5.65 veya 168.1.5.60-168.1.5.70 gibi isteklerin kabul edeceği IP adresini veya IP adresi aralığını belirtir.
Bu Aralık dahil.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Azure depolama tablosunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği tablo için bir SAS belirteci oluşturur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -İzin
Azure depolama tablosunun izinlerini belirtir.
Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -İlke
Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -İletişim kuralı
Bir istek için izin verilen protokolü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
* HttpsOnly
* HttpsOrHttp varsayılan değer HttpsOrHttp.

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartPartitionKey
Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç aralığının bölüm anahtarını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRowKey
Bu cmdlet 'in oluşturduğu belirteç için aralığın başlangıç satır anahtarını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Başlangıçsaati
SAS belirtecinin ne zaman geçerli olacağını belirtir.

```yaml
Type: System.Nullable`1[System.DateTime]
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext

## ÇıKıŞLAR

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorageContext](./New-AzureStorageContext.md)
