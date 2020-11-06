---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8b280a13e7eb7a2e6ea3f52b4a121f313504b2ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587067"
---
# New-AzureStorageAccountSASToken

## SYNOPSIS
Hesap düzeyi SAS belirteci oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Tanım
**New-AzureStorageSASToken** cmdlet 'i, bir Azure depolama hesabı için hesap düzeyi paylaşılan erişim IMZASı (SAS) oluşturur.

SAS belirtecini birden fazla hizmete yönelik izinler temsilci seçmek veya nesne düzeyinde SAS belirteciyle kullanılamayan hizmetlerin izinlerini temsil etmek için kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: tam izinli bir hesap düzeyi SAS belirteci oluşturma
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Bu komut tam izni olan bir hesap düzeyi SAS belirteci oluşturur.

### Örnek 2: bir IP adresleri aralığı için hesap düzeyi SAS belirteci oluşturma
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Bu komut, belirtilen IP adresi aralığından yalnızca HTTPS istekleri için bir hesap düzeyi SAS belirteci oluşturur.

## PARAMETRELERINE

### -Context
Azure depolama bağlamını belirtir.
**Azurestoragecontext** nesnesini almak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.

```yaml
Type: DateTime
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -İzin
Depolama hesabı izinlerini belirtir.
İzinler yalnızca belirtilen kaynak türüyle eşleşirse geçerlidir.
Kabul edilebilir izin değerleri hakkında daha fazla bilgi için bkz: hesap SA 'ları oluşturmahttps://go.microsoft.com/fwlink/?LinkId=799514

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

### -İletişim kuralı
Hesap SA 'larının verildiği bir istek için izin verilen protokolü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- HttpsOnly
- HttpsOrHttp

Varsayılan değer HttpsOrHttp değeridir.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
SAS belirteciyle kullanılabilen kaynak türlerini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Yabilirsiniz
- Hizmetinin
- Kapsayıcıdaki
- Nesnelerini

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hizmet
Hizmeti belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Yabilirsiniz
- 'Unu
- Dosyasý
- Kuyruğ
- Tablo

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Başlangıçsaati
SAS 'ın geçerli olacağı **Tarih saat** nesnesi olarak saat belirtir.
**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.

```yaml
Type: DateTime
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

### Istoragecontext

' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder

## ÇıKıŞLAR

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)

[New-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)

[New-AzureStorageQueueSASToken](./New-AzureStorageQueueSASToken.md)

[New-AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)

[New-AzureStorageTableSASToken](./New-AzureStorageTableSASToken.md)


