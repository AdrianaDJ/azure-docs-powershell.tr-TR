---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105321"
---
# Get-AzsEdgeGatewayPool

## SYNOPSIS


## INDEKI

### Liste (varsayılan)
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Al
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Getviaıdentity
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Tanım


## ÖRNEKLERDEN

### Örnek 1: tüm Edge ağ geçidi havuzlarının listesini alın.
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

Tüm Edge ağ geçidi havuzlarının bir listesini edinin.

### Örnek 2: belirli bir Edge ağ geçidi havuzu edinin.
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

Belirli bir Edge ağ geçidi havuzu edinin.

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

### -Filtre


```yaml
Type: System.String
Parameter Sets: List
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
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Konum


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Ad


```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionID


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıedgegatewaypool



## NOTLARıNDA

KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.

INPUTOBJECT <IFabricAdminIdentity> : 
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

## ILGILI BAĞLANTıLAR

