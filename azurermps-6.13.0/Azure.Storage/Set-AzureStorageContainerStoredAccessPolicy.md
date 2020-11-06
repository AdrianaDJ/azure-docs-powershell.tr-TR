---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6502183d97c92dba864e68942fae214591398f91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587355"
---
# Set-AzureStorageContainerStoredAccessPolicy

## SYNOPSIS
Azure depolama kapsayıcısı için depolanan bir erişim ilkesini ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Set-AzureStorageContainerStoredAccessPolicy** cmdlet 'i, bir Azure depolama kapsayıcısı için depolanan bir erişim ilkesini ayarlar.

## ÖRNEKLERDEN

### Örnek 1: tam izinli bir depolama kapsayıcısında depolanan erişim ilkesi ayarlama
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

Bu komut MyContainer adındaki depolama kapsayıcısı için Policy06 adlı bir erişim ilkesi ayarlar.

## PARAMETRELERINE

### -ClientTimeoutPerRequest
Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.
Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.
Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.

```yaml
Type: System.Nullable`1[System.Int32]
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
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Kapsayıcı
Azure depolama kapsayıcısı adını belirtir.

```yaml
Type: System.String
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

### -ExpiryTime
Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.

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

### -NoExpiryTime
Erişim ilkesinde son kullanma tarihi olmadığını gösterir.

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

### -NoStartTime
Başlangıç saatini $Null olarak ayarlar.

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

### -İzin
Depolanan erişim ilkesinde depolama kapsayıcısına erişim izinlerini belirtir.
Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.

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

### -İlke
Depolanan erişim ilkesinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.
Belirtilen aralıkta önceki çağrı başarısız olursa, bu cmdlet isteği yeniden dener.
Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Başlangıçsaati
Depolanan erişim ilkesinin geçerli olacağı saati belirtir.

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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

[Get-AzureStorageContainerStoredAccessPolicy](./Get-AzureStorageContainerStoredAccessPolicy.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)

[New-AzureStorageContainerStoredAccessPolicy](./New-AzureStorageContainerStoredAccessPolicy.md)

[Remove-AzureStorageContainerStoredAccessPolicy](./Remove-AzureStorageContainerStoredAccessPolicy.md)
