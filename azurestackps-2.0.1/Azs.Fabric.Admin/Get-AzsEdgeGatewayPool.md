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
# <span data-ttu-id="e3535-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="e3535-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="e3535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3535-102">SYNOPSIS</span></span>


## <span data-ttu-id="e3535-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3535-103">SYNTAX</span></span>

### <span data-ttu-id="e3535-104">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e3535-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e3535-105">Al</span><span class="sxs-lookup"><span data-stu-id="e3535-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e3535-106">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="e3535-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="e3535-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3535-107">DESCRIPTION</span></span>


## <span data-ttu-id="e3535-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3535-108">EXAMPLES</span></span>

### <span data-ttu-id="e3535-109">Örnek 1: tüm Edge ağ geçidi havuzlarının listesini alın.</span><span class="sxs-lookup"><span data-stu-id="e3535-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="e3535-110">Tüm Edge ağ geçidi havuzlarının bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="e3535-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="e3535-111">Örnek 2: belirli bir Edge ağ geçidi havuzu edinin.</span><span class="sxs-lookup"><span data-stu-id="e3535-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="e3535-112">Belirli bir Edge ağ geçidi havuzu edinin.</span><span class="sxs-lookup"><span data-stu-id="e3535-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="e3535-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3535-113">PARAMETERS</span></span>

### <span data-ttu-id="e3535-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3535-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="e3535-115">-Filtre</span><span class="sxs-lookup"><span data-stu-id="e3535-115">-Filter</span></span>


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

### <span data-ttu-id="e3535-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3535-116">-InputObject</span></span>
<span data-ttu-id="e3535-117">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e3535-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3535-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="e3535-118">-Location</span></span>


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

### <span data-ttu-id="e3535-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3535-119">-Name</span></span>


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

### <span data-ttu-id="e3535-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e3535-120">-PassThru</span></span>


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

### <span data-ttu-id="e3535-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3535-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="e3535-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e3535-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="e3535-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3535-123">CommonParameters</span></span>
<span data-ttu-id="e3535-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3535-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3535-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e3535-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3535-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3535-126">INPUTS</span></span>

### <span data-ttu-id="e3535-127">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="e3535-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="e3535-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3535-128">OUTPUTS</span></span>

### <span data-ttu-id="e3535-129">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıedgegatewaypool</span><span class="sxs-lookup"><span data-stu-id="e3535-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="e3535-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3535-130">NOTES</span></span>

<span data-ttu-id="e3535-131">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e3535-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3535-132">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3535-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e3535-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="e3535-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="e3535-134">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="e3535-135">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="e3535-136">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="e3535-137">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="e3535-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="e3535-138">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="e3535-139">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="e3535-140">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="e3535-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3535-141">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="e3535-142">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="e3535-143">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="e3535-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e3535-144">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="e3535-145">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="e3535-146">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="e3535-147">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e3535-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="e3535-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e3535-149">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="e3535-150">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="e3535-151">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="e3535-152">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="e3535-153">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="e3535-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e3535-154">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e3535-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e3535-155">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="e3535-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="e3535-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3535-156">RELATED LINKS</span></span>

