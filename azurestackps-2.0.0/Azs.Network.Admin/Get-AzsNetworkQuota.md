---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935989"
---
# <span data-ttu-id="566c5-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="566c5-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="566c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="566c5-102">SYNOPSIS</span></span>
<span data-ttu-id="566c5-103">Ada göre bir kota alın.</span><span class="sxs-lookup"><span data-stu-id="566c5-103">Get a quota by name.</span></span>

## <span data-ttu-id="566c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="566c5-104">SYNTAX</span></span>

### <span data-ttu-id="566c5-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="566c5-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="566c5-106">Al</span><span class="sxs-lookup"><span data-stu-id="566c5-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="566c5-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="566c5-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="566c5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="566c5-108">DESCRIPTION</span></span>
<span data-ttu-id="566c5-109">Tüm kotaları listeler.</span><span class="sxs-lookup"><span data-stu-id="566c5-109">List all quotas.</span></span>
<span data-ttu-id="566c5-110">Adı veya filtreyi geçirerek listeyi sınırlayın.</span><span class="sxs-lookup"><span data-stu-id="566c5-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="566c5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="566c5-111">EXAMPLES</span></span>

### <span data-ttu-id="566c5-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="566c5-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="566c5-113">Tüm ağ kotalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="566c5-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="566c5-114">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="566c5-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="566c5-115">Belirtilen ağ kotasını alır.</span><span class="sxs-lookup"><span data-stu-id="566c5-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="566c5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="566c5-116">PARAMETERS</span></span>

### <span data-ttu-id="566c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="566c5-117">-DefaultProfile</span></span>
<span data-ttu-id="566c5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="566c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="566c5-119">-Filtre</span><span class="sxs-lookup"><span data-stu-id="566c5-119">-Filter</span></span>
<span data-ttu-id="566c5-120">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="566c5-120">OData filter parameter.</span></span>

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

### <span data-ttu-id="566c5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="566c5-121">-InputObject</span></span>
<span data-ttu-id="566c5-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="566c5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="566c5-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="566c5-123">-Location</span></span>
<span data-ttu-id="566c5-124">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="566c5-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="566c5-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="566c5-125">-Name</span></span>
<span data-ttu-id="566c5-126">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="566c5-126">Name of the resource.</span></span>

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

### <span data-ttu-id="566c5-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="566c5-127">-PassThru</span></span>
<span data-ttu-id="566c5-128">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="566c5-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="566c5-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="566c5-129">-SubscriptionId</span></span>
<span data-ttu-id="566c5-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="566c5-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="566c5-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="566c5-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="566c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566c5-132">CommonParameters</span></span>
<span data-ttu-id="566c5-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="566c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566c5-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="566c5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566c5-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="566c5-135">INPUTS</span></span>

### <span data-ttu-id="566c5-136">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. ınetworkadminıdentity</span><span class="sxs-lookup"><span data-stu-id="566c5-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="566c5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="566c5-137">OUTPUTS</span></span>

### <span data-ttu-id="566c5-138">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. Api20150615. ıquota</span><span class="sxs-lookup"><span data-stu-id="566c5-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="566c5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="566c5-139">NOTES</span></span>

<span data-ttu-id="566c5-140">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="566c5-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="566c5-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="566c5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="566c5-142">INPUTOBJECT <INetworkAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="566c5-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="566c5-143">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="566c5-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="566c5-144">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="566c5-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="566c5-145">`[ResourceName <String>]`: Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="566c5-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="566c5-146">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="566c5-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="566c5-147">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="566c5-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="566c5-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="566c5-148">RELATED LINKS</span></span>

