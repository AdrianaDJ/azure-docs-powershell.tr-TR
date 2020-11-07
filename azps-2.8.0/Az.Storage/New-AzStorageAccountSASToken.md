---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 83480321e58d4dbd21d0a13dd6139c2f2d905c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934180"
---
# New-AzStorageAccountSASToken

## SYNOPSIS
Hesap düzeyi SAS belirteci oluşturur.

## INDEKI

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzStorageSASToken** cmdlet 'ı bir Azure depolama hesabı için hesap düzeyi paylaşılan erişim IMZASı (SAS) oluşturur.
SAS belirtecini birden fazla hizmete yönelik izinler temsilci seçmek veya nesne düzeyinde SAS belirteciyle kullanılamayan hizmetlerin izinlerini temsil etmek için kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: tam izinli bir hesap düzeyi SAS belirteci oluşturma
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Bu komut tam izni olan bir hesap düzeyi SAS belirteci oluşturur.

### Örnek 2: bir IP adresleri aralığı için hesap düzeyi SAS belirteci oluşturma
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Bu komut, belirtilen IP adresi aralığından yalnızca HTTPS istekleri için bir hesap düzeyi SAS belirteci oluşturur.

## PARAMETRELERINE

### -Context
Azure depolama bağlamını belirtir.
**Azurestoragecontext** nesnesini almak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Paylaşılan erişim imzasının geçersiz olacağı zamanı belirtir.

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

### -İzin
Depolama hesabı izinlerini belirtir.
İzinler yalnızca belirtilen kaynak türüyle eşleşirse geçerlidir.
Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.
Kabul edilebilir izin değerleri hakkında daha fazla bilgi için bkz: hesap SA 'ları oluşturma https://go.microsoft.com/fwlink/?LinkId=799514

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

### -İletişim kuralı
Hesap SA 'larının verildiği bir istek için izin verilen protokolü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- HttpsOnly
- HttpsOrHttp varsayılan değer HttpsOrHttp.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
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
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
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
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
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

### Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext

## ÇıKıŞLAR

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzStorageBlobSASToken](./New-AzStorageBlobSASToken.md)

[Yeni-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)

[Yeni-AzStorageFileSASToken](./New-AzStorageFileSASToken.md)

[Yeni-AzStorageQueueSASToken](./New-AzStorageQueueSASToken.md)

[Yeni-AzStorageShareSASToken](./New-AzStorageShareSASToken.md)

[Yeni-AzStorageTableSASToken](./New-AzStorageTableSASToken.md)


