---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936005"
---
# <span data-ttu-id="6129a-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="6129a-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="6129a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6129a-102">SYNOPSIS</span></span>
<span data-ttu-id="6129a-103">İstenen hizmet durumu nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6129a-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="6129a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6129a-104">SYNTAX</span></span>

### <span data-ttu-id="6129a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6129a-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6129a-106">Al</span><span class="sxs-lookup"><span data-stu-id="6129a-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6129a-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="6129a-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6129a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6129a-108">DESCRIPTION</span></span>
<span data-ttu-id="6129a-109">İstenen hizmet durumu nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6129a-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="6129a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6129a-110">EXAMPLES</span></span>

### <span data-ttu-id="6129a-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="6129a-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="6129a-112">Her hizmetin durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6129a-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="6129a-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="6129a-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="6129a-114">Hizmetin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="6129a-114">Returns a service's health.</span></span>

## <span data-ttu-id="6129a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6129a-115">PARAMETERS</span></span>

### <span data-ttu-id="6129a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6129a-116">-DefaultProfile</span></span>
<span data-ttu-id="6129a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6129a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6129a-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="6129a-118">-Filter</span></span>
<span data-ttu-id="6129a-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="6129a-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="6129a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6129a-120">-InputObject</span></span>
<span data-ttu-id="6129a-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6129a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6129a-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="6129a-122">-Location</span></span>
<span data-ttu-id="6129a-123">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="6129a-123">Name of the region</span></span>

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

### <span data-ttu-id="6129a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6129a-124">-ResourceGroupName</span></span>
<span data-ttu-id="6129a-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6129a-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="6129a-126">-Servicesağlık</span><span class="sxs-lookup"><span data-stu-id="6129a-126">-ServiceHealth</span></span>
<span data-ttu-id="6129a-127">Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="6129a-127">Service Health name.</span></span>

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

### <span data-ttu-id="6129a-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6129a-128">-SubscriptionId</span></span>
<span data-ttu-id="6129a-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="6129a-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6129a-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6129a-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6129a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6129a-131">CommonParameters</span></span>
<span data-ttu-id="6129a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6129a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6129a-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6129a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6129a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6129a-134">INPUTS</span></span>

### <span data-ttu-id="6129a-135">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6129a-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="6129a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6129a-136">OUTPUTS</span></span>

### <span data-ttu-id="6129a-137">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. Api20160501. Iservvoicehealth</span><span class="sxs-lookup"><span data-stu-id="6129a-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="6129a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6129a-138">NOTES</span></span>

<span data-ttu-id="6129a-139">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6129a-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6129a-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6129a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6129a-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="6129a-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6129a-142">`[AlertName <String>]`: Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="6129a-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="6129a-143">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="6129a-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6129a-144">`[Location <String>]`: Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="6129a-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="6129a-145">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6129a-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6129a-146">`[ResourceRegistrationId <String>]`: Kaynak kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6129a-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="6129a-147">`[ServiceHealth <String>]`: Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="6129a-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="6129a-148">`[ServiceRegistrationId <String>]`: Hizmet kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6129a-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="6129a-149">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="6129a-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6129a-150">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6129a-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6129a-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6129a-151">RELATED LINKS</span></span>
