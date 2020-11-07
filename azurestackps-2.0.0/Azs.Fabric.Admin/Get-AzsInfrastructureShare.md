---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937121"
---
# <span data-ttu-id="cb91f-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="cb91f-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="cb91f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb91f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb91f-103">İstenen doku dosyası paylaşımını döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb91f-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="cb91f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb91f-104">SYNTAX</span></span>

### <span data-ttu-id="cb91f-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb91f-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="cb91f-106">Al</span><span class="sxs-lookup"><span data-stu-id="cb91f-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cb91f-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="cb91f-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="cb91f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb91f-108">DESCRIPTION</span></span>
<span data-ttu-id="cb91f-109">İstenen doku dosyası paylaşımını döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb91f-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="cb91f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb91f-110">EXAMPLES</span></span>

### <span data-ttu-id="cb91f-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="cb91f-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="cb91f-112">Tüm dosya paylaşımlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb91f-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="cb91f-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="cb91f-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="cb91f-114">Ada dayalı bir dosya paylaşımı döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb91f-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="cb91f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb91f-115">PARAMETERS</span></span>

### <span data-ttu-id="cb91f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb91f-116">-DefaultProfile</span></span>
<span data-ttu-id="cb91f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb91f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb91f-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="cb91f-118">-Filter</span></span>
<span data-ttu-id="cb91f-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="cb91f-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="cb91f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb91f-120">-InputObject</span></span>
<span data-ttu-id="cb91f-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb91f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cb91f-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="cb91f-122">-Location</span></span>
<span data-ttu-id="cb91f-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="cb91f-123">Location of the resource.</span></span>

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

### <span data-ttu-id="cb91f-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb91f-124">-Name</span></span>
<span data-ttu-id="cb91f-125">Doku dosyası paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="cb91f-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cb91f-126">-PassThru</span></span>
<span data-ttu-id="cb91f-127">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="cb91f-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb91f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb91f-128">-ResourceGroupName</span></span>
<span data-ttu-id="cb91f-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="cb91f-130">-Atla</span><span class="sxs-lookup"><span data-stu-id="cb91f-130">-Skip</span></span>
<span data-ttu-id="cb91f-131">OData Skip parametresi.</span><span class="sxs-lookup"><span data-stu-id="cb91f-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="cb91f-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="cb91f-132">-SubscriptionId</span></span>
<span data-ttu-id="cb91f-133">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="cb91f-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb91f-134">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cb91f-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cb91f-135">-Üst</span><span class="sxs-lookup"><span data-stu-id="cb91f-135">-Top</span></span>
<span data-ttu-id="cb91f-136">OData üst parametresi.</span><span class="sxs-lookup"><span data-stu-id="cb91f-136">OData top parameter.</span></span>

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

### <span data-ttu-id="cb91f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb91f-137">CommonParameters</span></span>
<span data-ttu-id="cb91f-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb91f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb91f-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cb91f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb91f-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb91f-140">INPUTS</span></span>

### <span data-ttu-id="cb91f-141">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. ıfabricadminıdentity</span><span class="sxs-lookup"><span data-stu-id="cb91f-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cb91f-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb91f-142">OUTPUTS</span></span>

### <span data-ttu-id="cb91f-143">Microsoft. Azure. PowerShell. cmdlet. FabricAdmin. modeller. Api20160501. ıfileshare</span><span class="sxs-lookup"><span data-stu-id="cb91f-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="cb91f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb91f-144">NOTES</span></span>

<span data-ttu-id="cb91f-145">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cb91f-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb91f-146">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb91f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cb91f-147">INPUTOBJECT <IFabricAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="cb91f-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb91f-148">`[Drive <String>]`: Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cb91f-149">`[EdgeGateway <String>]`: Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cb91f-150">`[EdgeGatewayPool <String>]`: Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cb91f-151">`[FabricLocation <String>]`: Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="cb91f-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cb91f-152">`[FileShare <String>]`: Fabric dosya paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cb91f-153">`[IPPool <String>]`: IP havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cb91f-154">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="cb91f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb91f-155">`[InfraRole <String>]`: Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cb91f-156">`[InfraRoleInstance <String>]`: Altyapı rol örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cb91f-157">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="cb91f-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cb91f-158">`[LogicalNetwork <String>]`: Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cb91f-159">`[LogicalSubnet <String>]`: Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cb91f-160">`[MacAddressPool <String>]`: MAC adresi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cb91f-161">`[Operation <String>]`: İşlem tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cb91f-162">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cb91f-163">`[ScaleUnit <String>]`: Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cb91f-164">`[ScaleUnitNode <String>]`: Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cb91f-165">`[SlbMuxInstance <String>]`: SLB MUX örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cb91f-166">`[StorageSubSystem <String>]`: Depolama sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cb91f-167">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="cb91f-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cb91f-168">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cb91f-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cb91f-169">`[Volume <String>]`: Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="cb91f-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cb91f-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb91f-170">RELATED LINKS</span></span>

