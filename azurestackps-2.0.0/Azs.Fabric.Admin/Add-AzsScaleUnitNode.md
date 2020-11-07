---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937145"
---
# Add-AzsScaleUnitNode

## SYNOPSIS
Ölçek birimini ölçeklendirir.

## INDEKI

### Scalegenişletilen (varsayılan)
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Tonlama
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Scaleviaıdentity
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Scaleviaıdentitygenişletilmiş
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Ölçek birimini ölçeklendirir.

## ÖRNEKLERDEN

### Örnek 1: Add-AzsScaleUnitNode
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

Ölçek birimi kümeniz için yeni bir ölçek birimi düğümü ekleyin.

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

### -Awaitstorageyakınsama
Bayrak, işlemin dönmeden önce işlemin yakınsamasını bekleyip beklemediğini belirtir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
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

### -InputObject
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
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
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -NodeList
Ölçek birimindeki düğümlerin listesi.
Oluşturmak için, NODELIST özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
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
Kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -ScaleUnit
Ölçek birimlerinin adı.

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ScaleUnitNodeParameter
Ölçek birim düğümü kümesi eklemeye olanak tanıyan giriş verilerinin listesi.
Oluşturmak için, SCALEUNITNODEPARAMETER özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -SubscriptionID
Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.
Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
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

### Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. IScaleOutScaleUnitParametersList

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
  - `[StorageSubSystem <String>]`: Depolama sisteminin adı.
  - `[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.
  - `[Volume <String>]`: Depolama biriminin adı.

NODELIST <IScaleOutScaleUnitParameters [] >: ölçek birimindeki düğümlerin listesi.
  - `[BmciPv4Address <String>]`: Fiziksel makinenin BMC adresi.
  - `[ComputerName <String>]`: Fiziksel makinenin bilgisayar adı.

SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : ölçek birim düğümü kümesi eklemeye olanak tanıyan giriş verilerinin listesi.
  - `[AwaitStorageConvergence <Boolean?>]`: Bayrak işlemin dönmeden önce işlemin yakınsamasını bekleyip beklemediğini belirtir.
  - `[NodeList <IScaleOutScaleUnitParameters[]>]`: Ölçek birimindeki düğümlerin listesi.
    - `[BmciPv4Address <String>]`: Fiziksel makinenin BMC adresi.
    - `[ComputerName <String>]`: Fiziksel makinenin bilgisayar adı.

## ILGILI BAĞLANTıLAR

