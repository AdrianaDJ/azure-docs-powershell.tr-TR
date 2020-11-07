---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 2ffae1a1d12b503e478e18d57a31fffddd9c10a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752136"
---
# New-AzDeploymentManagerServiceTopology

## SYNOPSIS
Hizmet topolojisi oluşturur.

## INDEKI

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-AzDeploymentManagerServiceTopology** cmdlet 'i bir hizmet topolojisi oluşturur.

Döndürülen ServiceTopology nesnesini yerel olarak değiştirebilir ve Set-AzDeploymentManagerServiceTopology cmdlet 'ini kullanarak topolojiye değişiklikler uygulayabilirsiniz.
Döndürülen nesne 

Döndürülen nesnede, bu hizmet topolojisinde bildirilen hizmetlerin piyasaya dağıtılacağını göstermek için bir piyasaya çıkarma alanına başvurabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

Bu cmdlet, ContosoServiceTopology adını ve ABD Merkezi konumunu içeren ContosoResourceGroup kaynak grubunda yeni bir hizmet topolojisi oluşturur. Yapıt kaynağı RESOURCEID, bu topolojideki hizmet birimi tanımlarının gerektirdiği yapıların belirtilen yapıt kaynağından okunması gerektiğini belirtir.

### Örnek 2
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

Bu cmdlet, ContosoServiceTopology adını ve ABD Merkezi konumunu içeren ContosoResourceGroup kaynak grubunda yeni bir hizmet topolojisi oluşturur. Yapıt kaynak başvurusunun yokluğu, bu topolojideki hizmet birimi tanımları için gereken yapıların hizmet biriminde mutlak SAS URI olarak sağlandığını gösterir.

## PARAMETRELERINE

### -Artifactsource
Topoloji oluşturan yapıların depolandığı yapıt kaynağının tanıtıcısı.

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

### -Konum
Topolojinin konumu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Topolojinin adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Kaynak etiketlerini temsil eden karma bir tablo.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

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

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
