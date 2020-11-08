---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106709"
---
# <span data-ttu-id="ef0a9-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="ef0a9-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="ef0a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0a9-103">Bir bölgenin istenen sistem durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="ef0a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef0a9-104">SYNTAX</span></span>

### <span data-ttu-id="ef0a9-105">Get (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ef0a9-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef0a9-106">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="ef0a9-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef0a9-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="ef0a9-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ef0a9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef0a9-108">DESCRIPTION</span></span>
<span data-ttu-id="ef0a9-109">Bir bölgenin istenen sistem durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="ef0a9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef0a9-110">EXAMPLES</span></span>

### <span data-ttu-id="ef0a9-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="ef0a9-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="ef0a9-112">Bölgenin uygunluk durumu listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="ef0a9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef0a9-113">PARAMETERS</span></span>

### <span data-ttu-id="ef0a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0a9-114">-DefaultProfile</span></span>
<span data-ttu-id="ef0a9-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef0a9-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="ef0a9-116">-Filter</span></span>
<span data-ttu-id="ef0a9-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="ef0a9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef0a9-118">-InputObject</span></span>
<span data-ttu-id="ef0a9-119">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ef0a9-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="ef0a9-120">-Location</span></span>
<span data-ttu-id="ef0a9-121">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="ef0a9-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ef0a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef0a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef0a9-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef0a9-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ef0a9-124">-SubscriptionId</span></span>
<span data-ttu-id="ef0a9-125">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef0a9-126">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef0a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0a9-127">CommonParameters</span></span>
<span data-ttu-id="ef0a9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0a9-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0a9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef0a9-130">INPUTS</span></span>

### <span data-ttu-id="ef0a9-131">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ef0a9-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="ef0a9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef0a9-132">OUTPUTS</span></span>

### <span data-ttu-id="ef0a9-133">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. Api20160501. ıregionhealth</span><span class="sxs-lookup"><span data-stu-id="ef0a9-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="ef0a9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef0a9-134">NOTES</span></span>

<span data-ttu-id="ef0a9-135">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef0a9-136">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ef0a9-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ef0a9-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef0a9-138">`[AlertName <String>]`: Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="ef0a9-139">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ef0a9-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef0a9-140">`[Location <String>]`: Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="ef0a9-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="ef0a9-141">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ef0a9-142">`[ResourceRegistrationId <String>]`: Kaynak kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="ef0a9-143">`[ServiceHealth <String>]`: Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="ef0a9-144">`[ServiceRegistrationId <String>]`: Hizmet kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="ef0a9-145">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ef0a9-146">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ef0a9-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ef0a9-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef0a9-147">RELATED LINKS</span></span>

