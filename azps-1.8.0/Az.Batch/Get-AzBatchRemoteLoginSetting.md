---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 03c37bb1cf70dfefc5373e9211d6365feb133ad4
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761870"
---
# Get-AzBatchRemoteLoginSetting

## SYNOPSIS
İşlem düğümü için uzak oturum açma ayarlarını alır.

## INDEKI

### Kimlik (varsayılan)
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzBatchRemoteLoginSetting** cmdlet 'i, sanal makine altyapısına dayalı havuzda bir hesaplama düğümü için uzaktan oturum açma ayarlarını alır.

## ÖRNEKLERDEN

### Örnek 1: havuzdaki tüm düğümler için uzaktan oturum açma ayarlarını alma
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

İlk komut, **Get-AzBatchAccountKeys** kullanarak aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamı alır.
Komut, $Context değişkeninde bağlamı depolar ve sonraki komutta kullanılır.
İkinci komut, **Get-AzBatchComputeNode** kullanarak havuzdaki tüm COMPUTE düğümünü
Komut, ardışık düzen işlecini kullanarak her bilgisayar düğümünü geçerli cmdlet 'e geçirir.
Komut, her işlem düğümü için uzak oturum açma ayarlarını alır.

### Örnek 2: düğüm için uzak oturum açma ayarlarını alma
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

İlk komut, aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamını alır ve $Context değişkeninde depolar.
İkinci komut, KIMLIĞI etkileyen havuzda bulunan havuzda belirtilen KIMLIĞINE sahip olan COMPUTE düğümü için uzaktan oturum açma ayarlarını alır.

## PARAMETRELERINE

### -BatchContext
Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.
Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** edinmek için Get-AzBatchAccountKeys cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
Bu cmdlet 'in uzaktan oturum açma ayarlarını aldığı **PSComputeNode** nesnesi olarak bir COMPUTE düğümü belirtir.
Compute node nesnesi edinmek için Get-AzBatchComputeNode cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Computenodeıd
Uzaktan oturum açma ayarlarının alınacağı işlem düğümünün KIMLIĞINI belirtir.
Bu cmdlet 'in uzaktan oturum açma ayarlarını aldığı.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Sanal makineyi içeren havuzun KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: Id
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

### Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### Microsoft.Azure.Commands.Batch. Modeller. PSRemoteLoginSettings

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Aztopluaccountkeys](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchRemoteDesktopProtocolFile](./Get-AzBatchRemoteDesktopProtocolFile.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/az.batch)


