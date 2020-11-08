---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108266"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
VM 'e atanan "Konuk yapılandırması" türünde bir girişimin Konuk yapılandırma ilkesi durumlarını (ayrıntılı) alır.
Initiative, "Initiative" tanım türü ilkedir.

## INDEKI

### VmScope (varsayılan)
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Initivenamescope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Reporsscope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzVMGuestPolicyStatus cmdlet, VM 'e atanan "Konuk yapılandırması" türünde bir girişimin Konuk yapılandırma ilkesi durumlarını alır.
Initiative, "Initiative" tanım türü ilkedir.
Bu cmdlet, VM 'deki uyumluluk durumlarını ve girişimdeki bireysel ilkeler için uyumlu olmama nedenlerini alır.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

VM için tüm en son Konuk yapılandırma ilkesi durumlarını edinin.
Durum, uyumluluk için denetlenen kaynak bilgilerinin "Konuk yapılandırması" türündeki tüm girişimlerdeki her ilke için VM 'in uyumluluk durumunu içerir.
Sonuçlar en son durumları içerir, önceki geçmiş durumları içermez.

### Örnek 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

En son Konuk yapılandırması ilke durumlarını Initiative ID ile alın. Durum, girişimdeki her ilke için VM 'in uyumluluk durumunu, uyumluluk nedenlerini, uyumluluk denetiminin süresini, uyumluluk için denetlenen kaynak bilgilerini içerir.
Sonuçlar önceki durumların üretilmediğinden, girişimdeki her ilkeye ilişkin en son durumu içerir.

### Örnek 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

En son Konuk yapılandırması ilke durumlarını Initiative adına göre edinin.
Durum, girişimdeki her ilke için VM 'in uyumluluk durumunu, uyumluluk nedenlerini, uyumluluk denetiminin süresini, uyumluluk için denetlenen kaynak bilgilerini içerir.
Sonuçlar önceki durumların üretilmediğinden, girişimdeki her ilkeye ilişkin en son durumu içerir.

### Örnek 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

ReportId ile Konuk yapılandırma ilkesi durumunu edinin.
ReportId, initiativeId veya Initiative adına göre Get-AzVMGuestPolicyStatus sonuçlarında bulunan ReportId özelliğidir (lütfen diğer örneklere bakın)

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

### -InitiativeId
Tanımlama türünün Initiative ve category Konuk yapılandırması olduğu bir ilkenin tanım kimliği

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Initikavename
Tanımlama türünün Initiative ve category Konuk yapılandırması olduğu bir ilkenin adı

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportId
Konuk yapılandırma ilkesinin durumu.
Tanımlama türünün Initiative ve category olduğu bir ilke, durumları almak için bir kapsama atanmalıdır.

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
VM adı.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
## ÇıKıŞLAR

### Microsoft. Azure. Commands. GuestConfiguration. modeller. PolicyStatusDetailed
## NOTLARıNDA

## ILGILI BAĞLANTıLAR
