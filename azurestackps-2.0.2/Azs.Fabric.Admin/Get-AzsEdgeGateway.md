---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106625"
---
# <span data-ttu-id="51888-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="51888-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="51888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51888-102">SYNOPSIS</span></span>
<span data-ttu-id="51888-103">İstenen Edge ağ geçidini döndürür.</span><span class="sxs-lookup"><span data-stu-id="51888-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="51888-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51888-104">SYNTAX</span></span>

### <span data-ttu-id="51888-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51888-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="51888-106">Al</span><span class="sxs-lookup"><span data-stu-id="51888-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="51888-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="51888-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="51888-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="51888-108">DESCRIPTION</span></span>
<span data-ttu-id="51888-109">İstenen Edge ağ geçidini döndürür.</span><span class="sxs-lookup"><span data-stu-id="51888-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="51888-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51888-110">EXAMPLES</span></span>

### <span data-ttu-id="51888-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="51888-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="51888-112">Belirli bir konumdaki tüm kenar ağ geçitlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="51888-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="51888-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51888-113">PARAMETERS</span></span>

### <span data-ttu-id="51888-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51888-114">-DefaultProfile</span></span>
<span data-ttu-id="51888-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51888-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51888-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="51888-116">-Filter</span></span>
<span data-ttu-id="51888-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="51888-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="51888-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51888-118">-InputObject</span></span>
<span data-ttu-id="51888-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51888-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="51888-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="51888-120">-Location</span></span>
<span data-ttu-id="51888-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="51888-121">Location of the resource.</span></span>

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

### <span data-ttu-id="51888-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="51888-122">-Name</span></span>
<span data-ttu-id="51888-123">Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="51888-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="51888-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="51888-124">-PassThru</span></span>
<span data-ttu-id="51888-125">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="51888-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="51888-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51888-126">-ResourceGroupName</span></span>
<span data-ttu-id="51888-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="51888-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="51888-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="51888-128">-SubscriptionId</span></span>
<span data-ttu-id="51888-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="51888-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="51888-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="51888-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="51888-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51888-131">CommonParameters</span></span>
<span data-ttu-id="51888-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51888-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51888-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="51888-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51888-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51888-134">INPUTS</span></span>

### <span data-ttu-id="51888-135">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="51888-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="51888-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51888-136">OUTPUTS</span></span>

### <span data-ttu-id="51888-137">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıedgegateway</span><span class="sxs-lookup"><span data-stu-id="51888-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="51888-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51888-138">NOTES</span></span>

<span data-ttu-id="51888-139">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="51888-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51888-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51888-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="51888-141">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="51888-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51888-142">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="51888-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="51888-143">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="51888-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="51888-144">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="51888-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="51888-145">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="51888-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="51888-146">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="51888-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="51888-147">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="51888-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="51888-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="51888-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51888-149">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="51888-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="51888-150">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="51888-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="51888-151">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="51888-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="51888-152">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="51888-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="51888-153">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="51888-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="51888-154">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="51888-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="51888-155">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="51888-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="51888-156">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="51888-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="51888-157">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="51888-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="51888-158">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="51888-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="51888-159">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="51888-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="51888-160">`[StoragePool <String>]`: Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="51888-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="51888-161">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="51888-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="51888-162">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="51888-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="51888-163">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="51888-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="51888-164">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="51888-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="51888-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51888-165">RELATED LINKS</span></span>

