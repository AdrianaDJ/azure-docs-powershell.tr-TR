---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: d6bb118a6b7699672209618e1409fe6a9bed466d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106710"
---
# Disable-AzsInfrastructureRoleInstance

## SYNOPSIS


## INDEKI

### Kapatma (varsayılan)
```
Disable-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### Shutdownviaıdentity
```
Disable-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Bakım için bir altyapı rolü örneğini kapatma.

## ÖRNEKLERDEN

### Örnek 1:
```powershell
PS C:\> Disable-AzsInfrastructureRoleInstance -Name "n22r0903-Xrp03"

Shutdown an infrastructure role instance for maintenance.
```

Bakım için bir altyapı rolü örneğini kapatma.


## PARAMETRELERINE

### -Iş
Komutu iş olarak çalıştırmak

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
Onayınızı sorma.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Konum
Kaynağın konumu.

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Ad
Altyapı rolü örneğinin adı.

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -NoWait
Komutu zaman uyumsuz olarak çalıştırır

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
Kaynak sağlayıcının kaydedildiği kaynak grubu.

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionID
Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.
Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: Shutdown
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

### Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity

## ÇıKıŞLAR

### System. Boolean



## NOTLARıNDA

KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.

INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi
  - `[Drive <String>]`: Depolama sürücüsünün adı.
  - `[EdgeGateway <String>]`: Uç ağ geçidinin adı.
  - `[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.
  - `[FabricLocation <String>]`: Doku konumu.
  - `[FileShare <String>]`: Fabric dosya paylaşım adı.
  - `[IPPool <String>]`: IP havuzu adı.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[InfraRole <String>]`: Altyapı rolü adı.
  - `[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.
  - `[Location <String>]`: Kaynağın konumu.
  - `[LogicalNetwork <String>]`: Mantıksal ağın adı.
  - `[LogicalSubnet <String>]`: Mantıksal alt ağın adı.
  - `[MacAddressPool <String>]`: MAC adresi havuzunun adı.
  - `[Operation <String>]`: İşlem tanımlayıcısı.
  - `[ResourceGroupName <String>]`: Kaynak grubunun adı.
  - `[ScaleUnit <String>]`: Ölçek birimlerinin adı.
  - `[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.
  - `[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.
  - `[StoragePool <String>]`: Depolama havuzu adı.
  - `[StorageSubSystem <String>]`: Depolama sisteminin adı.
  - `[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.
  - `[Volume <String>]`: Depolama biriminin adı.

## ILGILI BAĞLANTıLAR

