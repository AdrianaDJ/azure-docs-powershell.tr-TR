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
# <span data-ttu-id="27dd2-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="27dd2-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="27dd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="27dd2-103">İstenen IP havuzunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="27dd2-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="27dd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27dd2-104">SYNTAX</span></span>

### <span data-ttu-id="27dd2-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27dd2-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="27dd2-106">Al</span><span class="sxs-lookup"><span data-stu-id="27dd2-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="27dd2-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="27dd2-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="27dd2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="27dd2-108">DESCRIPTION</span></span>
<span data-ttu-id="27dd2-109">İstenen IP havuzunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="27dd2-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="27dd2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27dd2-110">EXAMPLES</span></span>

### <span data-ttu-id="27dd2-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="27dd2-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="27dd2-112">Tüm altyapı IP havuzlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="27dd2-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="27dd2-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="27dd2-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="27dd2-114">Ada dayalı bir altyapı IP havuzu edinin.</span><span class="sxs-lookup"><span data-stu-id="27dd2-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="27dd2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27dd2-115">PARAMETERS</span></span>

### <span data-ttu-id="27dd2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27dd2-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="27dd2-117">-Filtre</span><span class="sxs-lookup"><span data-stu-id="27dd2-117">-Filter</span></span>
<span data-ttu-id="27dd2-118">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="27dd2-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="27dd2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27dd2-119">-InputObject</span></span>
<span data-ttu-id="27dd2-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27dd2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="27dd2-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="27dd2-121">-Location</span></span>
<span data-ttu-id="27dd2-122">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="27dd2-122">Location of the resource.</span></span>

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

### <span data-ttu-id="27dd2-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="27dd2-123">-Name</span></span>
<span data-ttu-id="27dd2-124">IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-124">IP pool name.</span></span>

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

### <span data-ttu-id="27dd2-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="27dd2-125">-PassThru</span></span>
<span data-ttu-id="27dd2-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="27dd2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="27dd2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27dd2-127">-ResourceGroupName</span></span>
<span data-ttu-id="27dd2-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="27dd2-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="27dd2-129">-SubscriptionId</span></span>
<span data-ttu-id="27dd2-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="27dd2-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="27dd2-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="27dd2-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="27dd2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27dd2-132">CommonParameters</span></span>
<span data-ttu-id="27dd2-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27dd2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27dd2-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="27dd2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27dd2-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27dd2-135">INPUTS</span></span>

### <span data-ttu-id="27dd2-136">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="27dd2-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="27dd2-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27dd2-137">OUTPUTS</span></span>

### <span data-ttu-id="27dd2-138">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıippool</span><span class="sxs-lookup"><span data-stu-id="27dd2-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="27dd2-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27dd2-139">NOTES</span></span>

<span data-ttu-id="27dd2-140">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="27dd2-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27dd2-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="27dd2-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="27dd2-142">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="27dd2-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="27dd2-143">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="27dd2-144">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="27dd2-145">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="27dd2-146">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="27dd2-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="27dd2-147">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="27dd2-148">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="27dd2-149">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="27dd2-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="27dd2-150">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="27dd2-151">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="27dd2-152">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="27dd2-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="27dd2-153">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="27dd2-154">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="27dd2-155">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="27dd2-156">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="27dd2-157">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="27dd2-158">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="27dd2-159">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="27dd2-160">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="27dd2-161">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="27dd2-162">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="27dd2-163">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="27dd2-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="27dd2-164">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="27dd2-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="27dd2-165">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="27dd2-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="27dd2-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27dd2-166">RELATED LINKS</span></span>

