---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935203"
---
# Remove-AzsSubscription

## SYNOPSIS


## INDEKI

### Sil (varsayılan)
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### Deleteviaıdentity
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım


## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

Belirtilen aboneliği silin.

## PARAMETRELERINE

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Force


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

### -InputObject
Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Geçiş


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

### -SubscriptionID


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. ıubscriptionıdentity

## ÇıKıŞLAR

### System. Boolean



## NOTLARıNDA

KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.

INPUTOBJECT <ISubscriptionIdentity> : 
  - `[DelegatedProviderId <String>]`: Temsilci seçilen sağlayıcının kimliği.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[OfferName <String>]`: Teklifin adı.
  - `[SubscriptionId <String>]`: Aboneliğin kimliği.

## ILGILI BAĞLANTıLAR

