---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 174353aacbfe939294f654a4f5f61548bfc672dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595063"
---
# Get-AzureStorageContainerStoredAccessPolicy

## SYNOPSIS
Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorageContainerStoredAccessPolicy** cmdlet 'ı, Azure depolama kapsayıcısı için depolanan erişim ilkesini veya ilkelerini listeler.

## ÖRNEKLERDEN

### Örnek 1: depolama kapsayıcısında depolanan bir erişim ilkesi alma
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

Bu komut, Container07 adındaki depolama kapsayıcısında Policy22 adındaki erişim ilkesini alır.

### Örnek 2: depolama kapsayıcısındaki tüm depolanan erişim ilkelerini alma
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

Bu komut, Container07 adlı depolama kapsayıcısındaki tüm erişim ilkelerini alır.

## PARAMETRELERINE

### -ClientTimeoutPerRequest
Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.
Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.
Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Maksimum eşzamanlı ağ çağrılarını belirtir.
Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.
Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.
Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.
Varsayılan değer 10 ' dır.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Kapsayıcı
Azure depolama kapsayıcının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Context
Azure depolama bağlamını belirtir.

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

### -İlke
Azure depolanan erişim ilkesini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.
Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.

```yaml
Type: Int32
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

### Dizisi

Parametre ' Container ', ardışık düzenin ' String ' türünün değerini kabul eder

### Istoragecontext

' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Windowsazde. Storage. blob. SharedAccessBlobPolicy

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorageContainerStoredAccessPolicy](./New-AzureStorageContainerStoredAccessPolicy.md)

[Remove-AzureStorageContainerStoredAccessPolicy](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[Set-AzureStorageContainerStoredAccessPolicy](./Set-AzureStorageContainerStoredAccessPolicy.md)


