---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 7b0cdf0cbe0aecdb2e1b6829ed1ec22b1e485e92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320002"
---
# Remove-AzWvdHostPool

## SYNOPSIS
Konak havuzunu kaldırma.

## INDEKI

### Sil (varsayılan)
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Deleteviaıdentity
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Konak havuzunu kaldırma.

## ÖRNEKLERDEN

### Örnek 1: Windows sanal masaüstü HostPool adını adıyla silme
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

Bu komut, kaynak grubundaki Windows sanal masaüstü HostPool öğesini siler.

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

### -Force
Force bayrağı sessionHost öğesini siler.

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
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Belirtilen kaynak grubundaki konak havuzunun adı

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

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
Kaynak grubunun adı.
Ad büyük/küçük harfe duyarlıdır.

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
Hedef aboneliğin KIMLIĞI.

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

### Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi
  - `[ApplicationGroupName <String>]`: Uygulama grubunun adı
  - `[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı
  - `[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı
  - `[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[ResourceGroupName <String>]`: Kaynak grubunun adı. Ad büyük/küçük harfe duyarlıdır.
  - `[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı
  - `[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.
  - `[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı
  - `[WorkspaceName <String>]`: Çalışma alanının adı

## ILGILI BAĞLANTıLAR

