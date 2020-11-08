---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106969"
---
# Get-AzsIPPool

## SYNOPSIS
İstenen IP havuzunu döndürür.

## INDEKI

### Liste (varsayılan)
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Al
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Getviaıdentity
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Tanım
İstenen IP havuzunu döndürür.

## ÖRNEKLERDEN

### Örnek 1: 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

Tüm altyapı IP havuzlarını edinin.

### Örnek 2: 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

Ada dayalı bir altyapı IP havuzu edinin.

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
OData filtre parametresi.

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
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

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
Kaynağın konumu.

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
IP havuzu adı.

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
Parameter Sets: Get, List
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

### Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıippool



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

