---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936009"
---
# <span data-ttu-id="8e493-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="8e493-101">Close-AzsAlert</span></span>

## <span data-ttu-id="8e493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e493-102">SYNOPSIS</span></span>
<span data-ttu-id="8e493-103">Verilen uyarıyı kapatır.</span><span class="sxs-lookup"><span data-stu-id="8e493-103">Closes the given alert.</span></span>

## <span data-ttu-id="8e493-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e493-104">SYNTAX</span></span>

### <span data-ttu-id="8e493-105">Genişletme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e493-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e493-106">Kapanması</span><span class="sxs-lookup"><span data-stu-id="8e493-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8e493-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e493-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e493-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8e493-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e493-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e493-109">DESCRIPTION</span></span>
<span data-ttu-id="8e493-110">Verilen uyarıyı kapatır.</span><span class="sxs-lookup"><span data-stu-id="8e493-110">Closes the given alert.</span></span>

## <span data-ttu-id="8e493-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e493-111">EXAMPLES</span></span>

### <span data-ttu-id="8e493-112">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="8e493-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="8e493-113">Bir uyarıyı ada göre kapatma.</span><span class="sxs-lookup"><span data-stu-id="8e493-113">Close an alert by Name.</span></span>

### <span data-ttu-id="8e493-114">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="8e493-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="8e493-115">Bir uyarıyı boru aracılığıyla kapatma.</span><span class="sxs-lookup"><span data-stu-id="8e493-115">Close an alert through piping.</span></span>

## <span data-ttu-id="8e493-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e493-116">PARAMETERS</span></span>

### <span data-ttu-id="8e493-117">-Uyarı</span><span class="sxs-lookup"><span data-stu-id="8e493-117">-Alert</span></span>
<span data-ttu-id="8e493-118">Bu nesne bir uyarı kaynağını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="8e493-118">This object represents an alert resource.</span></span>
<span data-ttu-id="8e493-119">Oluşturmak için, uyarı özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8e493-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="8e493-120">-AlertId</span></span>
<span data-ttu-id="8e493-121">Uyarının KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="8e493-122">-AlertProperty</span></span>
<span data-ttu-id="8e493-123">Uyarının özellikleri.</span><span class="sxs-lookup"><span data-stu-id="8e493-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-124">-Closevseçbyuseralias</span><span class="sxs-lookup"><span data-stu-id="8e493-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="8e493-125">Uyarıyı kapatan Kullanıcı diğer adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-126">-Closevseçtimestamp</span><span class="sxs-lookup"><span data-stu-id="8e493-126">-ClosedTimestamp</span></span>
<span data-ttu-id="8e493-127">Uyarı kapatıldığında zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="8e493-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="8e493-128">-CreatedTimestamp</span></span>
<span data-ttu-id="8e493-129">Uyarı oluşturulduğunda zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="8e493-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e493-130">-DefaultProfile</span></span>
<span data-ttu-id="8e493-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e493-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e493-132">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="8e493-132">-Description</span></span>
<span data-ttu-id="8e493-133">Uyarının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="8e493-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="8e493-134">-FaultId</span></span>
<span data-ttu-id="8e493-135">Uyarının hata KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-136">-Faulttypeıd</span><span class="sxs-lookup"><span data-stu-id="8e493-136">-FaultTypeId</span></span>
<span data-ttu-id="8e493-137">Uyarının hata türü KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-138">-Hasvalidçözüm Ationaction</span><span class="sxs-lookup"><span data-stu-id="8e493-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="8e493-139">Uyarının düzeltildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e493-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-140">-Impactedresourcedisplayname</span><span class="sxs-lookup"><span data-stu-id="8e493-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="8e493-141">Etkilenen öğenin görünen adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-142">-Impactedresourceıd</span><span class="sxs-lookup"><span data-stu-id="8e493-142">-ImpactedResourceId</span></span>
<span data-ttu-id="8e493-143">Etkilenen öğenin kaynak KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e493-144">-InputObject</span></span>
<span data-ttu-id="8e493-145">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e493-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="8e493-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="8e493-147">Uyarının en son güncelleştirildiği zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="8e493-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-148">-Konum</span><span class="sxs-lookup"><span data-stu-id="8e493-148">-Location</span></span>
<span data-ttu-id="8e493-149">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="8e493-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="8e493-150">-Location1</span></span>
<span data-ttu-id="8e493-151">Kaynağın yaşadığı Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="8e493-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-152">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e493-152">-Name</span></span>
<span data-ttu-id="8e493-153">Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-154">-Düzeltme</span><span class="sxs-lookup"><span data-stu-id="8e493-154">-Remediation</span></span>
<span data-ttu-id="8e493-155">Uyarı için yönetici dostu düzeltme yönergelerini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e493-156">-ResourceGroupName</span></span>
<span data-ttu-id="8e493-157">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-158">-Resourceproviderregistrationıd</span><span class="sxs-lookup"><span data-stu-id="8e493-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="8e493-159">Uyarının ait olduğu hizmetin kayıt KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-160">-Resourceregistrationıd</span><span class="sxs-lookup"><span data-stu-id="8e493-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="8e493-161">Uyarıyla ilişkili kaynağın kayıt KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="8e493-162">Uyarı bir kaynakla ilişkilendirildiyse, kaynak kayıt KIMLIĞI null olur.</span><span class="sxs-lookup"><span data-stu-id="8e493-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-163">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="8e493-163">-Severity</span></span>
<span data-ttu-id="8e493-164">Uyarının önem derecesi.</span><span class="sxs-lookup"><span data-stu-id="8e493-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-165">Durumlu</span><span class="sxs-lookup"><span data-stu-id="8e493-165">-State</span></span>
<span data-ttu-id="8e493-166">Uyarının durumu.</span><span class="sxs-lookup"><span data-stu-id="8e493-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-167">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8e493-167">-SubscriptionId</span></span>
<span data-ttu-id="8e493-168">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="8e493-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e493-169">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8e493-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-170">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8e493-170">-Tag</span></span>
<span data-ttu-id="8e493-171">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="8e493-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-172">-Başlık</span><span class="sxs-lookup"><span data-stu-id="8e493-172">-Title</span></span>
<span data-ttu-id="8e493-173">Etkilenen öğenin kaynak KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-174">-Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="8e493-174">-User</span></span>
<span data-ttu-id="8e493-175">İşlemi gerçekleştirmek için kullanılan Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-175">The username used to perform the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-176">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e493-176">-Confirm</span></span>
<span data-ttu-id="8e493-177">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e493-177">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e493-178">-WhatIf</span></span>
<span data-ttu-id="8e493-179">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e493-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e493-180">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e493-180">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e493-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e493-181">CommonParameters</span></span>
<span data-ttu-id="8e493-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e493-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e493-183">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8e493-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e493-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e493-184">INPUTS</span></span>

### <span data-ttu-id="8e493-185">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. Api20160501. ıalert</span><span class="sxs-lookup"><span data-stu-id="8e493-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="8e493-186">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8e493-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="8e493-187">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e493-187">OUTPUTS</span></span>

### <span data-ttu-id="8e493-188">Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. Api20160501. ıalert</span><span class="sxs-lookup"><span data-stu-id="8e493-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="8e493-189">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e493-189">NOTES</span></span>

<span data-ttu-id="8e493-190">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8e493-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e493-191">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e493-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8e493-192">Uyarı <IAlert> : Bu nesne bir uyarı kaynağını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="8e493-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="8e493-193">`[Location <String>]`: Kaynağın bulunduğu Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="8e493-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="8e493-194">`[Tag <ITrackedResourceTags>]`: Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="8e493-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="8e493-195">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e493-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8e493-196">`[AlertId <String>]`: Uyarının KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="8e493-197">`[AlertProperty <IAlertModelAlertProperties>]`: Uyarının özellikleri.</span><span class="sxs-lookup"><span data-stu-id="8e493-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="8e493-198">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e493-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8e493-199">`[ClosedByUserAlias <String>]`: Uyarıyı kapatan Kullanıcı diğer adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="8e493-200">`[ClosedTimestamp <String>]`: Uyarı kapatıldığında zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="8e493-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="8e493-201">`[CreatedTimestamp <String>]`: Uyarı oluşturulduğunda zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="8e493-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="8e493-202">`[Description <IDictionary[]>]`: Uyarının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="8e493-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="8e493-203">`[FaultId <String>]`: Uyarının hata KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="8e493-204">`[FaultTypeId <String>]`: Uyarının hata türü KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="8e493-205">`[HasValidRemediationAction <Boolean?>]`: Uyarının düzeltildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e493-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="8e493-206">`[ImpactedResourceDisplayName <String>]`: Etkilenen öğenin görünen adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="8e493-207">`[ImpactedResourceId <String>]`: Etkilenen öğenin kaynak KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="8e493-208">`[LastUpdatedTimestamp <String>]`: Uyarının en son güncelleştirildiği zaman zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="8e493-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="8e493-209">`[Remediation <IDictionary[]>]`: Uyarı için yönetici dostu düzeltme yönergelerini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="8e493-210">`[ResourceProviderRegistrationId <String>]`: Uyarının ait olduğu hizmetin kayıt KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="8e493-211">`[ResourceRegistrationId <String>]`: Uyarıyla ilişkili kaynağın kayıt KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="8e493-212">Uyarı bir kaynakla ilişkilendirildiyse, kaynak kayıt KIMLIĞI null olur.</span><span class="sxs-lookup"><span data-stu-id="8e493-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="8e493-213">`[Severity <String>]`: Uyarının önem derecesi.</span><span class="sxs-lookup"><span data-stu-id="8e493-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="8e493-214">`[State <String>]`: Uyarının durumu.</span><span class="sxs-lookup"><span data-stu-id="8e493-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="8e493-215">`[Title <String>]`: Etkilenen öğenin kaynak KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8e493-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="8e493-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="8e493-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e493-217">`[AlertName <String>]`: Uyarının adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="8e493-218">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="8e493-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e493-219">`[Location <String>]`: Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="8e493-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="8e493-220">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8e493-221">`[ResourceRegistrationId <String>]`: Kaynak kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8e493-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="8e493-222">`[ServiceHealth <String>]`: Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="8e493-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="8e493-223">`[ServiceRegistrationId <String>]`: Hizmet kayıt KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8e493-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="8e493-224">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="8e493-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8e493-225">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8e493-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8e493-226">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e493-226">RELATED LINKS</span></span>

