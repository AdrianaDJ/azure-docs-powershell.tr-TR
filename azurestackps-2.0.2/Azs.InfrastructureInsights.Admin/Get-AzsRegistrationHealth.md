---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106706"
---
# <span data-ttu-id="5e7bb-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="5e7bb-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="5e7bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7bb-103">Kaynak hakkında istenen sistem durumu bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="5e7bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e7bb-104">SYNTAX</span></span>

### <span data-ttu-id="5e7bb-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e7bb-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e7bb-106">Al</span><span class="sxs-lookup"><span data-stu-id="5e7bb-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e7bb-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="5e7bb-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5e7bb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e7bb-108">DESCRIPTION</span></span>
<span data-ttu-id="5e7bb-109">Kaynak hakkında istenen sistem durumu bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="5e7bb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e7bb-110">EXAMPLES</span></span>

### <span data-ttu-id="5e7bb-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="5e7bb-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="5e7bb-112">Her kaynağın bir hizmet altındaki durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="5e7bb-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="5e7bb-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="5e7bb-114">Bir Microsoft. Fabric. admin için, sistem durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="5e7bb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e7bb-115">PARAMETERS</span></span>

### <span data-ttu-id="5e7bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7bb-116">-DefaultProfile</span></span>
<span data-ttu-id="5e7bb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e7bb-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="5e7bb-118">-Filter</span></span>
<span data-ttu-id="5e7bb-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5e7bb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e7bb-120">-InputObject</span></span>
<span data-ttu-id="5e7bb-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e7bb-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="5e7bb-122">-Location</span></span>
<span data-ttu-id="5e7bb-123">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="5e7bb-123">Name of the region</span></span>

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

### <span data-ttu-id="5e7bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e7bb-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e7bb-126">-Resourceregistrationıd</span><span class="sxs-lookup"><span data-stu-id="5e7bb-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="5e7bb-127">Kaynak kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="5e7bb-128">-Serviceregistrationıd</span><span class="sxs-lookup"><span data-stu-id="5e7bb-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="5e7bb-129">Hizmet kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-129">Service registration ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5e7bb-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5e7bb-130">-SubscriptionId</span></span>
<span data-ttu-id="5e7bb-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5e7bb-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5e7bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7bb-133">CommonParameters</span></span>
<span data-ttu-id="5e7bb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7bb-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7bb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e7bb-136">INPUTS</span></span>

### <span data-ttu-id="5e7bb-137">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5e7bb-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="5e7bb-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e7bb-138">OUTPUTS</span></span>

### <span data-ttu-id="5e7bb-139">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. Api20160501. ıresourcesağlık</span><span class="sxs-lookup"><span data-stu-id="5e7bb-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="5e7bb-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e7bb-140">NOTES</span></span>

<span data-ttu-id="5e7bb-141">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e7bb-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5e7bb-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="5e7bb-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e7bb-144">`[AlertName <String>]`: Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="5e7bb-145">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="5e7bb-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e7bb-146">`[Location <String>]`: Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="5e7bb-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="5e7bb-147">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5e7bb-148">`[ResourceRegistrationId <String>]`: Kaynak kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="5e7bb-149">`[ServiceHealth <String>]`: Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="5e7bb-150">`[ServiceRegistrationId <String>]`: Hizmet kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="5e7bb-151">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5e7bb-152">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5e7bb-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e7bb-153">RELATED LINKS</span></span>

