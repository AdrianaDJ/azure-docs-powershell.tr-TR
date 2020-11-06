---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8c16d52db3b2a1606cbab5999a8a165466fcdb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593875"
---
# Set-AzureStorageContainerAcl

## SYNOPSIS
Bir depolama kapsayıcısına genel erişim iznini ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Tanım
**Set-AzureStorageContainerAcl** cmdlet 'i, genel erişim iznini Azure 'da belirtilen depolama kapsayıcısına ayarlar.

## ÖRNEKLERDEN

### Örnek 1: Azure depolama kapsayıcısı ACL 'sini ada göre ayarlama
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

Bu komut, genel erişimi olmayan bir kapsayıcı oluşturur.

### Örnek 2: ardışık düzeni kullanarak Azure depolama kapsayıcısı ACL 'sini ayarlama
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

Bu komut, adı konteynerle başlayan tüm depolama kapsayıcılarını alır ve ardından tüm bunları blob erişimine izin verecek şekilde sonucu ardışık düzene geçirir.

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

### -Context
Azure depolama bağlamını belirtir.
Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.

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

### -Ad
Kapsayıcı adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Geçiş
Çalıştığınız öğeyi temsil eden bir nesne döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

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

### -İzin
Bu kapsayıcıya genel erişim düzeyini belirtir.
Varsayılan olarak, kapsayıcı ve içindeki blob 'lar yalnızca depolama hesabının sahibi tarafından erişilebilir.
Anonim kullanıcılara bir kapsayıcıya ve BLOB kullanıcılarına okuma izinleri vermek için, kapsayıcı izinlerini genel erişimi etkinleştirecek şekilde ayarlayabilirsiniz.
Anonim kullanıcılar, isteği doğrulamadan, genel kullanıma yönelik kapsayıcıda blob okuyabilir.
Bu parametre için kabul edilebilir değerler şunlardır:

--Container.
Bir kapsayıcıya ve blobilerine tam okuma erişimi sağlar.
İstemciler, anonim istek aracılığıyla kapsayıcıdaki blob 'ları numaralandırır, ancak depolama hesabındaki kapsayıcıları numaralandıramaz. --BLOB.
Anonim istek aracılığıyla kapsayıcıda blob verilerine okuma erişimi sağlar, ancak kapsayıcı verilerine erişim sağlamaz.
İstemciler anonim istek kullanılarak kapsayıcıdaki blob 'ları numaralandıramaz. --Off.
Erişimi yalnızca depolama hesabı sahibine kısıtlar.

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
İsteğin saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.
Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.
Her istek için sunucu tarafı zaman aşımı.

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

### Istoragecontext

' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder

### Dizisi

' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageContainer

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorageContainer](./Get-AzureStorageContainer.md)

[New-AzureStorageContainer](./New-AzureStorageContainer.md)

[Remove-AzureStorageContainer](./Remove-AzureStorageContainer.md)


