---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108567"
---
# Get-AzSynapseLinkedService

## SYNOPSIS
Çalışma alanındaki bağlantılı hizmetler hakkında bilgi alır.

## INDEKI

### GetByName (varsayılan)
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByObject
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzSynapseLinkedService** cmdlet 'i çalışma alanındaki bağlantılı hizmetler hakkında bilgi alır.
Bağlantılı hizmetin adını belirtirseniz, bu cmdlet bu bağlantılı hizmet hakkında bilgi alır.
Bir ad belirtmezseniz, bu cmdlet çalışma alanındaki bağlantılı hizmetler hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

Bu komut, ContosoWorkspace adlı çalışma alanındaki bağlantılı hizmetler hakkında bilgi alır.

### Örnek 2
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

Bu komut, ContosoWorkspace adındaki çalışma alanında ContosoLinkedService adındaki bağlantılı hizmetle ilgili bilgileri alır.

### Örnek 3
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

Bu komut, ContosoLinkedService adındaki bağlantılı hizmetle ilgili olarak, ContosoWorkspace aracılığıyla Contosoçalışma alanında bulunan bir bilgi alır.

## PARAMETRELERINE

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

### -Ad
Bağlantılı hizmet adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Çalışmaalanıadı
SYNAPSE çalışma alanının adı.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -
genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace

## ÇıKıŞLAR

### Microsoft. Azure. Commands. SYNAPSE. modeller. PSLinkedServiceResource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
