---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d1534c7cfacbcc70c2fe822676d67142401f9ff9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106630"
---
# <span data-ttu-id="230fe-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="230fe-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="230fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="230fe-102">SYNOPSIS</span></span>


## <span data-ttu-id="230fe-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="230fe-103">SYNTAX</span></span>

### <span data-ttu-id="230fe-104">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="230fe-104">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="230fe-105">Al</span><span class="sxs-lookup"><span data-stu-id="230fe-105">Get</span></span>
```
Get-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="230fe-106">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="230fe-106">GetViaIdentity</span></span>
```
Get-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="230fe-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="230fe-107">DESCRIPTION</span></span>


## <span data-ttu-id="230fe-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="230fe-108">EXAMPLES</span></span>

### <span data-ttu-id="230fe-109">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="230fe-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode

A list of all scale unit nodes at a location.
```

<span data-ttu-id="230fe-110">Bir konumdaki tüm ölçek birim düğümlerini alın.</span><span class="sxs-lookup"><span data-stu-id="230fe-110">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="230fe-111">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="230fe-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode -Name "HC1n25r2231"

A specific scale unit node at a location given a name.
```

<span data-ttu-id="230fe-112">Bir ad verilen konumda belirli bir ölçek birimi düğümünü edinin.</span><span class="sxs-lookup"><span data-stu-id="230fe-112">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="230fe-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="230fe-113">PARAMETERS</span></span>

### <span data-ttu-id="230fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="230fe-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="230fe-115">-Filtre</span><span class="sxs-lookup"><span data-stu-id="230fe-115">-Filter</span></span>


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

### <span data-ttu-id="230fe-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="230fe-116">-InputObject</span></span>
<span data-ttu-id="230fe-117">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="230fe-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="230fe-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="230fe-118">-Location</span></span>


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

### <span data-ttu-id="230fe-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="230fe-119">-Name</span></span>


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

### <span data-ttu-id="230fe-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="230fe-120">-PassThru</span></span>


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

### <span data-ttu-id="230fe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="230fe-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="230fe-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="230fe-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="230fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="230fe-123">CommonParameters</span></span>
<span data-ttu-id="230fe-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="230fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="230fe-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="230fe-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="230fe-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="230fe-126">INPUTS</span></span>

### <span data-ttu-id="230fe-127">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="230fe-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="230fe-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="230fe-128">OUTPUTS</span></span>

### <span data-ttu-id="230fe-129">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. IScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="230fe-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnitNode</span></span>



## <span data-ttu-id="230fe-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="230fe-130">NOTES</span></span>

<span data-ttu-id="230fe-131">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="230fe-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="230fe-132">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="230fe-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="230fe-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="230fe-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="230fe-134">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="230fe-135">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="230fe-136">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="230fe-137">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="230fe-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="230fe-138">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="230fe-139">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="230fe-140">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="230fe-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="230fe-141">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="230fe-142">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="230fe-143">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="230fe-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="230fe-144">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="230fe-145">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="230fe-146">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="230fe-147">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="230fe-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="230fe-148">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="230fe-149">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="230fe-150">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="230fe-151">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="230fe-152">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="230fe-153">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="230fe-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="230fe-154">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="230fe-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="230fe-155">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="230fe-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="230fe-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="230fe-156">RELATED LINKS</span></span>

