---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsmanifest
schema: 2.0.0
ms.openlocfilehash: 4e5ccedc67af31c19d35e5a91fad62ba46535ed7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106998"
---
# <span data-ttu-id="ddffd-101">Get-AzsManifest</span><span class="sxs-lookup"><span data-stu-id="ddffd-101">Get-AzsManifest</span></span>

## <span data-ttu-id="ddffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddffd-102">SYNOPSIS</span></span>
<span data-ttu-id="ddffd-103">Belirtilen bildirime ulaşın.</span><span class="sxs-lookup"><span data-stu-id="ddffd-103">Get the specified manifest.</span></span>

## <span data-ttu-id="ddffd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddffd-104">SYNTAX</span></span>

### <span data-ttu-id="ddffd-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ddffd-105">List (Default)</span></span>
```
Get-AzsManifest [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ddffd-106">Al</span><span class="sxs-lookup"><span data-stu-id="ddffd-106">Get</span></span>
```
Get-AzsManifest -ManifestName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddffd-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="ddffd-107">GetViaIdentity</span></span>
```
Get-AzsManifest -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ddffd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddffd-108">DESCRIPTION</span></span>
<span data-ttu-id="ddffd-109">Belirtilen bildirime ulaşın.</span><span class="sxs-lookup"><span data-stu-id="ddffd-109">Get the specified manifest.</span></span>

## <span data-ttu-id="ddffd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddffd-110">EXAMPLES</span></span>

### <span data-ttu-id="ddffd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ddffd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsManifest

Name     : Microsoft-Authorization-Admin--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata

Name     : Microsoft-Authorization--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata
```

<span data-ttu-id="ddffd-112">Geçerli aboneliğin altındaki tüm bildirimleri listeler.</span><span class="sxs-lookup"><span data-stu-id="ddffd-112">Lists all the manifests under the current subscription.</span></span>

## <span data-ttu-id="ddffd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddffd-113">PARAMETERS</span></span>

### <span data-ttu-id="ddffd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddffd-114">-DefaultProfile</span></span>
<span data-ttu-id="ddffd-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddffd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddffd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddffd-116">-InputObject</span></span>
<span data-ttu-id="ddffd-117">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ddffd-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ddffd-118">-ManifestName</span><span class="sxs-lookup"><span data-stu-id="ddffd-118">-ManifestName</span></span>
<span data-ttu-id="ddffd-119">Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-119">The manifest name.</span></span>

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

### <span data-ttu-id="ddffd-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ddffd-120">-SubscriptionId</span></span>
<span data-ttu-id="ddffd-121">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ddffd-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ddffd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddffd-122">CommonParameters</span></span>
<span data-ttu-id="ddffd-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddffd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddffd-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ddffd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddffd-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddffd-125">INPUTS</span></span>

### <span data-ttu-id="ddffd-126">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. ısubscriptionsadminıdentity</span><span class="sxs-lookup"><span data-stu-id="ddffd-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="ddffd-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddffd-127">OUTPUTS</span></span>

### <span data-ttu-id="ddffd-128">Microsoft. Azure. PowerShell. cmdlet. SubscriptionsAdmin. modeller. Api20151101. Sananifest</span><span class="sxs-lookup"><span data-stu-id="ddffd-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IManifest</span></span>

<span data-ttu-id="ddffd-129">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ddffd-129">ALIASES</span></span>

## <span data-ttu-id="ddffd-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddffd-130">NOTES</span></span>

<span data-ttu-id="ddffd-131">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ddffd-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ddffd-132">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ddffd-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ddffd-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="ddffd-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ddffd-134">`[DelegatedProvider <String>]`: Delegatedpprovider tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="ddffd-135">`[DelegatedProviderSubscriptionId <String>]`: Temsilci sağlayıcı abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="ddffd-136">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="ddffd-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ddffd-137">`[Location <String>]`: AzureStack konumu.</span><span class="sxs-lookup"><span data-stu-id="ddffd-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="ddffd-138">`[ManifestName <String>]`: Bildirim adı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="ddffd-139">`[Offer <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="ddffd-140">`[OfferDelegationName <String>]`: Teklif temsilcisinin adı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="ddffd-141">`[OperationsStatusName <String>]`: İşlem durumu adı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="ddffd-142">`[Plan <String>]`: Planın adı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="ddffd-143">`[PlanAcquisitionId <String>]`: Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="ddffd-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="ddffd-144">`[Quota <String>]`: Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="ddffd-145">`[ResourceGroupName <String>]`: Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="ddffd-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="ddffd-146">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ddffd-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ddffd-147">`[TargetSubscriptionId <String>]`: Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ddffd-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="ddffd-148">`[Tenant <String>]`: Dizin kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="ddffd-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="ddffd-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddffd-149">RELATED LINKS</span></span>

