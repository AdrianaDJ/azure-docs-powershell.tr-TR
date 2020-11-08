---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106771"
---
# <span data-ttu-id="d82bb-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="d82bb-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="d82bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d82bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d82bb-103">İstenen doku konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="d82bb-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="d82bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d82bb-104">SYNTAX</span></span>

### <span data-ttu-id="d82bb-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d82bb-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d82bb-106">Al</span><span class="sxs-lookup"><span data-stu-id="d82bb-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d82bb-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="d82bb-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="d82bb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d82bb-108">DESCRIPTION</span></span>
<span data-ttu-id="d82bb-109">İstenen doku konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="d82bb-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="d82bb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d82bb-110">EXAMPLES</span></span>

### <span data-ttu-id="d82bb-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="d82bb-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="d82bb-112">Tüm doku konumlarının bir listesini alın.</span><span class="sxs-lookup"><span data-stu-id="d82bb-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="d82bb-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="d82bb-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="d82bb-114">Ada göre bir konum alın.</span><span class="sxs-lookup"><span data-stu-id="d82bb-114">Get a location based on the name.</span></span>

## <span data-ttu-id="d82bb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d82bb-115">PARAMETERS</span></span>

### <span data-ttu-id="d82bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d82bb-116">-DefaultProfile</span></span>
<span data-ttu-id="d82bb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d82bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d82bb-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="d82bb-118">-FabricLocation</span></span>
<span data-ttu-id="d82bb-119">Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="d82bb-119">Fabric location.</span></span>

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

### <span data-ttu-id="d82bb-120">-Filtre</span><span class="sxs-lookup"><span data-stu-id="d82bb-120">-Filter</span></span>
<span data-ttu-id="d82bb-121">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="d82bb-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="d82bb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d82bb-122">-InputObject</span></span>
<span data-ttu-id="d82bb-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d82bb-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d82bb-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d82bb-124">-PassThru</span></span>
<span data-ttu-id="d82bb-125">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="d82bb-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d82bb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d82bb-126">-ResourceGroupName</span></span>
<span data-ttu-id="d82bb-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="d82bb-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d82bb-128">-SubscriptionId</span></span>
<span data-ttu-id="d82bb-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d82bb-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d82bb-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d82bb-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d82bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d82bb-131">CommonParameters</span></span>
<span data-ttu-id="d82bb-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d82bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d82bb-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d82bb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d82bb-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d82bb-134">INPUTS</span></span>

### <span data-ttu-id="d82bb-135">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="d82bb-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="d82bb-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d82bb-136">OUTPUTS</span></span>

### <span data-ttu-id="d82bb-137">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıfabriclocation</span><span class="sxs-lookup"><span data-stu-id="d82bb-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="d82bb-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d82bb-138">NOTES</span></span>

<span data-ttu-id="d82bb-139">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d82bb-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d82bb-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d82bb-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d82bb-141">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d82bb-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d82bb-142">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="d82bb-143">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="d82bb-144">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="d82bb-145">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="d82bb-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="d82bb-146">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="d82bb-147">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="d82bb-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d82bb-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d82bb-149">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="d82bb-150">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="d82bb-151">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="d82bb-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d82bb-152">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="d82bb-153">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="d82bb-154">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="d82bb-155">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="d82bb-156">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d82bb-157">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="d82bb-158">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="d82bb-159">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="d82bb-160">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="d82bb-161">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d82bb-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d82bb-162">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d82bb-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d82bb-163">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="d82bb-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="d82bb-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d82bb-164">RELATED LINKS</span></span>

