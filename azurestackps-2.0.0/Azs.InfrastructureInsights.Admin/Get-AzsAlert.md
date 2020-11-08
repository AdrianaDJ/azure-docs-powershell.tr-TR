---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937107"
---
# <span data-ttu-id="30856-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="30856-101">Get-AzsAlert</span></span>

## <span data-ttu-id="30856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30856-102">SYNOPSIS</span></span>
<span data-ttu-id="30856-103">İstenen uyarıyı döndürür.</span><span class="sxs-lookup"><span data-stu-id="30856-103">Returns the requested alert.</span></span>

## <span data-ttu-id="30856-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30856-104">SYNTAX</span></span>

### <span data-ttu-id="30856-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="30856-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="30856-106">Al</span><span class="sxs-lookup"><span data-stu-id="30856-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="30856-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="30856-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="30856-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="30856-108">DESCRIPTION</span></span>
<span data-ttu-id="30856-109">İstenen uyarıyı döndürür.</span><span class="sxs-lookup"><span data-stu-id="30856-109">Returns the requested alert.</span></span>

## <span data-ttu-id="30856-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30856-110">EXAMPLES</span></span>

### <span data-ttu-id="30856-111">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="30856-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="30856-112">Ada göre bir uyarı alın.</span><span class="sxs-lookup"><span data-stu-id="30856-112">Get an alert by Name.</span></span>

### <span data-ttu-id="30856-113">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="30856-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="30856-114">Tüm etkin uyarıları alın ve hata ve unvanlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="30856-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="30856-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30856-115">PARAMETERS</span></span>

### <span data-ttu-id="30856-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30856-116">-DefaultProfile</span></span>
<span data-ttu-id="30856-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30856-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30856-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="30856-118">-Filter</span></span>
<span data-ttu-id="30856-119">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="30856-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="30856-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30856-120">-InputObject</span></span>
<span data-ttu-id="30856-121">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30856-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="30856-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="30856-122">-Location</span></span>
<span data-ttu-id="30856-123">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="30856-123">Name of the region</span></span>

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

### <span data-ttu-id="30856-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="30856-124">-Name</span></span>
<span data-ttu-id="30856-125">Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="30856-125">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30856-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30856-126">-ResourceGroupName</span></span>
<span data-ttu-id="30856-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="30856-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="30856-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="30856-128">-SubscriptionId</span></span>
<span data-ttu-id="30856-129">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="30856-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="30856-130">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="30856-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="30856-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30856-131">CommonParameters</span></span>
<span data-ttu-id="30856-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30856-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30856-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="30856-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30856-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30856-134">INPUTS</span></span>

### <span data-ttu-id="30856-135">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="30856-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="30856-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30856-136">OUTPUTS</span></span>

### <span data-ttu-id="30856-137">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. Api20160501. ıalert</span><span class="sxs-lookup"><span data-stu-id="30856-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="30856-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30856-138">NOTES</span></span>

<span data-ttu-id="30856-139">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="30856-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30856-140">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30856-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="30856-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="30856-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30856-142">`[AlertName <String>]`: Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="30856-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="30856-143">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="30856-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30856-144">`[Location <String>]`: Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="30856-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="30856-145">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="30856-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="30856-146">`[ResourceRegistrationId <String>]`: Kaynak kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="30856-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="30856-147">`[ServiceHealth <String>]`: Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="30856-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="30856-148">`[ServiceRegistrationId <String>]`: Hizmet kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="30856-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="30856-149">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="30856-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="30856-150">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="30856-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="30856-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30856-151">RELATED LINKS</span></span>
