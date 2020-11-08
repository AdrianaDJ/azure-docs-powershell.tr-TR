---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106733"
---
# <span data-ttu-id="244e3-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="244e3-101">Get-AzsLocation</span></span>

## <span data-ttu-id="244e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="244e3-102">SYNOPSIS</span></span>
<span data-ttu-id="244e3-103">Belirtilen konumu edinin.</span><span class="sxs-lookup"><span data-stu-id="244e3-103">Get the specified location.</span></span>

## <span data-ttu-id="244e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="244e3-104">SYNTAX</span></span>

### <span data-ttu-id="244e3-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="244e3-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="244e3-106">Al</span><span class="sxs-lookup"><span data-stu-id="244e3-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="244e3-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="244e3-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="244e3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="244e3-108">DESCRIPTION</span></span>
<span data-ttu-id="244e3-109">Belirtilen konumu edinin.</span><span class="sxs-lookup"><span data-stu-id="244e3-109">Get the specified location.</span></span>

## <span data-ttu-id="244e3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="244e3-110">EXAMPLES</span></span>

### <span data-ttu-id="244e3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="244e3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="244e3-112">Tüm AzureStack konumlarının bir listesini alın.</span><span class="sxs-lookup"><span data-stu-id="244e3-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="244e3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="244e3-113">PARAMETERS</span></span>

### <span data-ttu-id="244e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="244e3-114">-DefaultProfile</span></span>
<span data-ttu-id="244e3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="244e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="244e3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="244e3-116">-InputObject</span></span>
<span data-ttu-id="244e3-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="244e3-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="244e3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="244e3-118">-Name</span></span>
<span data-ttu-id="244e3-119">AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="244e3-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="244e3-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="244e3-120">-SubscriptionId</span></span>
<span data-ttu-id="244e3-121">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="244e3-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="244e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="244e3-122">CommonParameters</span></span>
<span data-ttu-id="244e3-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="244e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="244e3-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="244e3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="244e3-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="244e3-125">INPUTS</span></span>

### <span data-ttu-id="244e3-126">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="244e3-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="244e3-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="244e3-127">OUTPUTS</span></span>

### <span data-ttu-id="244e3-128">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101.</span><span class="sxs-lookup"><span data-stu-id="244e3-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="244e3-129">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="244e3-129">ALIASES</span></span>

## <span data-ttu-id="244e3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="244e3-130">NOTES</span></span>

<span data-ttu-id="244e3-131">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="244e3-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="244e3-132">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="244e3-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="244e3-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="244e3-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="244e3-134">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="244e3-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="244e3-135">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="244e3-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="244e3-136">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="244e3-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="244e3-137">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="244e3-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="244e3-138">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="244e3-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="244e3-139">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="244e3-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="244e3-140">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="244e3-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="244e3-141">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="244e3-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="244e3-142">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="244e3-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="244e3-143">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="244e3-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="244e3-144">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="244e3-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="244e3-145">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="244e3-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="244e3-146">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="244e3-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="244e3-147">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="244e3-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="244e3-148">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="244e3-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="244e3-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="244e3-149">RELATED LINKS</span></span>

