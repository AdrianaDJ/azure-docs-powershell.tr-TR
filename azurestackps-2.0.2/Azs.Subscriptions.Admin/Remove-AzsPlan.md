---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplan
schema: 2.0.0
ms.openlocfilehash: fca0ab39b587bea05228da3a053fd1575b3e7e98
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106928"
---
# Remove-AzsPlan

## SYNOPSIS
Belirtilen planı silme.

## INDEKI

### Sil (varsayılan)
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Deleteviaıdentity
```
Remove-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## Tanım
Belirtilen planı silme.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Remove-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

```

Belirtilen planı silme

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -InputObject
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Ad
Planın adı.

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

### -Geçiş
Komut başarılı olduğunda doğru verir

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

### -ResourceGroupName
Kaynağın altında bulunduğu kaynak grubu.

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

### -SubscriptionID
Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity

## ÇıKıŞLAR

### System. Boolean

DIĞER adları

## NOTLARıNDA

KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.

INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi
  - `[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.
  - `[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[Location <String>]`: AzureStack konumu.
  - `[ManifestName <String>]`: Bildirim adı.
  - `[Offer <String>]`: Teklifin adı.
  - `[OfferDelegationName <String>]`: Teklif temsilcisinin adı.
  - `[OperationsStatusName <String>]`: İşlem durumu adı.
  - `[Plan <String>]`: Planın adı.
  - `[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı
  - `[Quota <String>]`: Kotanın adı.
  - `[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.
  - `[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.
  - `[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.
  - `[Tenant <String>]`: Dizin kiracı adı.

## ILGILI BAĞLANTıLAR

