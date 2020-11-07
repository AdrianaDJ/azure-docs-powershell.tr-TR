---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalnetwork
schema: 2.0.0
ms.openlocfilehash: 8229e487cd7c616969e049bbbea0ba7a6a18a448
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937122"
---
# <span data-ttu-id="00aff-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="00aff-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="00aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00aff-102">SYNOPSIS</span></span>
<span data-ttu-id="00aff-103">İstenen mantıksal ağı döndürür.</span><span class="sxs-lookup"><span data-stu-id="00aff-103">Returns the requested logical network.</span></span>

## <span data-ttu-id="00aff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00aff-104">SYNTAX</span></span>

### <span data-ttu-id="00aff-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="00aff-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="00aff-106">Al</span><span class="sxs-lookup"><span data-stu-id="00aff-106">Get</span></span>
```
Get-AzsLogicalNetwork -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="00aff-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="00aff-107">GetViaIdentity</span></span>
```
Get-AzsLogicalNetwork -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="00aff-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="00aff-108">DESCRIPTION</span></span>
<span data-ttu-id="00aff-109">İstenen mantıksal ağı döndürür.</span><span class="sxs-lookup"><span data-stu-id="00aff-109">Returns the requested logical network.</span></span>

## <span data-ttu-id="00aff-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00aff-110">EXAMPLES</span></span>

### <span data-ttu-id="00aff-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="00aff-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="00aff-112">Tüm mantıksal ağları bir yerde alın.</span><span class="sxs-lookup"><span data-stu-id="00aff-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="00aff-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="00aff-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A specific logical networks at a location based on a name.
```

<span data-ttu-id="00aff-114">Bir ad temelinde belirli bir yerde belirli bir mantıksal ağ edinin.</span><span class="sxs-lookup"><span data-stu-id="00aff-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="00aff-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00aff-115">PARAMETERS</span></span>

### <span data-ttu-id="00aff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00aff-116">-DefaultProfile</span></span>
<span data-ttu-id="00aff-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00aff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00aff-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="00aff-118">-Filter</span></span>
<span data-ttu-id="00aff-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="00aff-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="00aff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00aff-120">-InputObject</span></span>
<span data-ttu-id="00aff-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00aff-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="00aff-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="00aff-122">-Location</span></span>
<span data-ttu-id="00aff-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="00aff-123">Location of the resource.</span></span>

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

### <span data-ttu-id="00aff-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="00aff-124">-Name</span></span>
<span data-ttu-id="00aff-125">Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-125">Name of the logical network.</span></span>

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

### <span data-ttu-id="00aff-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="00aff-126">-PassThru</span></span>
<span data-ttu-id="00aff-127">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="00aff-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="00aff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00aff-128">-ResourceGroupName</span></span>
<span data-ttu-id="00aff-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="00aff-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="00aff-130">-SubscriptionId</span></span>
<span data-ttu-id="00aff-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="00aff-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="00aff-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="00aff-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="00aff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00aff-133">CommonParameters</span></span>
<span data-ttu-id="00aff-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00aff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00aff-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="00aff-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00aff-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00aff-136">INPUTS</span></span>

### <span data-ttu-id="00aff-137">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="00aff-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="00aff-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00aff-138">OUTPUTS</span></span>

### <span data-ttu-id="00aff-139">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ılogicalnetwork</span><span class="sxs-lookup"><span data-stu-id="00aff-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalNetwork</span></span>



## <span data-ttu-id="00aff-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00aff-140">NOTES</span></span>

<span data-ttu-id="00aff-141">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="00aff-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00aff-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="00aff-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="00aff-143">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="00aff-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00aff-144">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="00aff-145">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="00aff-146">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="00aff-147">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="00aff-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="00aff-148">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="00aff-149">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="00aff-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="00aff-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00aff-151">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="00aff-152">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="00aff-153">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="00aff-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="00aff-154">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="00aff-155">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="00aff-156">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="00aff-157">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="00aff-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="00aff-158">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="00aff-159">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="00aff-160">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="00aff-161">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="00aff-162">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="00aff-163">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="00aff-164">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="00aff-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="00aff-165">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="00aff-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="00aff-166">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="00aff-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="00aff-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00aff-167">RELATED LINKS</span></span>

