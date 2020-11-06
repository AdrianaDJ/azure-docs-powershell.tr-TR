---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 2a147e00dba480a483b10843b17347145a1dc2a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587692"
---
# Get-AzureBatchRemoteDesktopProtocolFile

## SYNOPSIS
İşlem düğümünden RDP dosyası alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Id_Path (varsayılan)
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Id_Stream
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Path
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureBatchRemoteDesktopProtocolFile** cmdlet 'i, bir Işlem düğümünden Uzak Masaüstü Protokolü (RDP) dosyası alır ve bunu dosya veya Kullanıcı tarafından sağlanan bir akışa kaydeder.

## ÖRNEKLERDEN

### Örnek 1: belirtilen işlem düğümünden RDP dosyası alma ve dosyayı kaydetme
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

Bu komut, ComputeNode01 kimlik Pool06 olan havuzda KIMLIĞI olan bir RDP dosyası alır.
Komut. rdp dosyasını C:\powershell\mycomputenode.rdpolarak kaydeder.
$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.

### Örnek 2: bir işlem düğümünden RDP dosyası alın ve kanalı kullanarak dosyayı kaydedin.
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

Bu komut, ComputeNode02 kimliğine sahip havuzda KIMLIK Pool06 olan COMPUTE düğümünü alır.
Komut bu işlem düğümünü ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.
Geçerli cmdlet, COMPUTE düğümünden bir. rpd dosyası alır ve içeriği C:\powershell\mycomputenode02.rdpadlı bir dosya olarak kaydeder.

### Örnek 3: belirtilen işlem düğümünden RDP dosyası alın ve bunu bir akışa yönlendirin
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.

İkinci komut, KIMLIĞI Pool06 olan havuzda KIMLIK ComputeNode03 olan COMPUTE düğümünden bir. rdp dosyası alır.
Komut dosya içeriğini $Stream akışa yönlendirir.

## PARAMETRELERINE

### -BatchContext
Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.
BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır. Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın. Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır. Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
**PSComputeNode** nesnesi olarak,. rdp dosyasının işaret ettiğini belirten bir COMPUTE düğümü belirtir.
Compute node nesnesi edinmek için Get-AzureBatchComputeNode cmdlet 'ini kullanın.

```yaml
Type: PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Computenodeıd
. Rdp dosyasının işaret olduğu COMPUTE düğümünün KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPath
Bu cmdlet 'in. rdp dosyasını kaydettiği dosya yolunu belirtir.

```yaml
Type: String
Parameter Sets: Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Bu cmdlet 'in RDP verilerini yönlendirdiği akışı belirtir.
Bu cmdlet bu akışı kapatmaz veya geri sarmaz.

```yaml
Type: Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Bu cmdlet 'in bir. rdp dosyası aldığı COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### BatchAccountContext
' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder

### PSComputeNode
' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchComputeNode](./Get-AzureBatchComputeNode.md)

[Azure toplu Iş cmdlet 'Leri](./AzureRM.Batch.md)


