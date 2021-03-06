---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 7328eda5e6821b7c403bf949460747fbf7d215e7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761930"
---
# Get-AzOperationalInsightsWorkspaceSharedKey

## SYNOPSIS
Çalışma alanı için paylaşılan anahtarları alır.

## INDEKI

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet 'i bir çalışma alanının paylaşılan anahtarlarını listeler.
Bu tuşlar, Işlemsel Öngörüler aracılarını çalışma alanına bağlamak için kullanılır.

## ÖRNEKLERDEN

### Örnek 1: paylaşılan anahtarları çalışma alanı adına göre alma
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı çalışma alanı için paylaşılan anahtarları alır.

### Örnek 2: ardışık düzeni kullanarak paylaşılan anahtarları alma
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

Bu komut, MyWorkspace adındaki çalışma alanını Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanarak alır ve çalışma alanını **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet 'ine geçirir.
Komut, bu çalışma alanı için paylaşılan anahtarları alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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
Çalışma alanı adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bir Azure Kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Operationalınsights. modeller. PSWorkspaceKeys

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure Operasyonel Öngörüler cmdlet 'Leri](/powershell/module/az.operationalinsights)

[Get-Azoperationalınsightsworkspace](./Get-AzOperationalInsightsWorkspace.md)


