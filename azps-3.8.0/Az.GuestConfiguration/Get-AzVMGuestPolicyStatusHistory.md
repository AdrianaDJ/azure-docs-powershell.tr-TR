---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096630"
---
# Get-AzVMGuestPolicyStatusHistory

## SYNOPSIS
VM 'e atanan "Konuk yapılandırması" türündeki bir girişimin Konuk yapılandırma ilkesi uyumluluk durumu geçmişini alır.
Initiative, "Initiative" tanım türü ilkedir.

## INDEKI

### Initivenamescope (varsayılan)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzVMGuestPolicyStatusHistory cmdlet, VM 'e atanan "Konuk yapılandırması" türündeki bir girişimin uyumluluk durumu geçmişini alır.
Initiative, "Initiative" tanım türü ilkedir.
Get-AzVMGuestPolicyStatusHistory cmdlet 'inin çıktısında bulunan ReportId kullanarak tek bir uyumluluk durumunun ayrıntılarını almak için Get-AzVMGuestPolicyStatus cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Uyumsuzluk kimliğine göre uyumluluk durumu geçmişini alır. ShowOnlyChange anahtarı yalnızca geçmiş durumu değişikliklerini gösterir.
İki uyumluluk çeki arasında değişmeyen durumları atlar.

### Örnek 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Uyumluluk durumu geçmişini Initiative adına göre alır.
ShowOnlyChange anahtarı yalnızca geçmiş durumu değişikliklerini gösterir.
İki uyumluluk çeki arasında değişmeyen durumları atlar.

### Örnek 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

VM 'ye atanan tüm konuk yapılandırma ilkelerinin uyumluluk durumu geçmişini alır.
ShowOnlyChange anahtarı yalnızca geçmiş durumu değişikliklerini gösterir.
İki uyumluluk çeki arasında değişmeyen durumları atlar.

### Örnek 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Uyumluluk durumu geçmişini Initiative ID 'ye göre alır.

### Örnek 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Uyumluluk durumu geçmişini Initiative adına göre alır.

### Örnek 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
VM 'ye atanan tüm konuk yapılandırma ilkelerinin uyumluluk durumu geçmişini alır.

### Örnek 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

ReportId ile Konuk yapılandırma ilkesi durumunu edinin.
ReportId, Get-Azvmguestpolicypolicy geçmiş sonuçlarında bulunabilir. (lütfen diğer örneklere bakın)

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

Required: False
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

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOnlyChange
Yalnızca Konuk yapılandırma ilkeleri için geçmiş durumu değişikliklerini gösterir.
İki uyumluluk durumu denetimi çalışması arasında değişmeyen durumları atlar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
VM adı.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
## ÇıKıŞLAR

### Microsoft. Azure. Commands. GuestConfiguration. modeller. PolicyStatus
## NOTLARıNDA

## ILGILI BAĞLANTıLAR
