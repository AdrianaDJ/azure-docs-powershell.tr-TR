---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279280"
---
# <span data-ttu-id="181dd-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="181dd-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="181dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="181dd-102">SYNOPSIS</span></span>
<span data-ttu-id="181dd-103">Belirtilen ortamda bir erişim ilkesi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="181dd-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="181dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="181dd-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="181dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="181dd-105">DESCRIPTION</span></span>
<span data-ttu-id="181dd-106">Belirtilen ortamda bir erişim ilkesi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="181dd-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="181dd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="181dd-107">EXAMPLES</span></span>

### <span data-ttu-id="181dd-108">Örnek 1: belirtilen bir ortamda erişim ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="181dd-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="181dd-109">Bu komut, belirli bir ortam için bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="181dd-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="181dd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="181dd-110">PARAMETERS</span></span>

### <span data-ttu-id="181dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181dd-111">-DefaultProfile</span></span>
<span data-ttu-id="181dd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="181dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="181dd-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="181dd-113">-Description</span></span>
<span data-ttu-id="181dd-114">Access ilkesinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="181dd-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="181dd-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="181dd-115">-EnvironmentName</span></span>
<span data-ttu-id="181dd-116">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="181dd-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="181dd-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="181dd-117">-Name</span></span>
<span data-ttu-id="181dd-118">Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="181dd-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181dd-119">-Sprincipalobjectid</span><span class="sxs-lookup"><span data-stu-id="181dd-119">-PrincipalObjectId</span></span>
<span data-ttu-id="181dd-120">Azure Active Directory 'de anaparanın ObjectID.</span><span class="sxs-lookup"><span data-stu-id="181dd-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="181dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="181dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="181dd-122">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="181dd-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="181dd-123">-Role</span><span class="sxs-lookup"><span data-stu-id="181dd-123">-Role</span></span>
<span data-ttu-id="181dd-124">Anapara atanan rollerin listesi.</span><span class="sxs-lookup"><span data-stu-id="181dd-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181dd-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="181dd-125">-SubscriptionId</span></span>
<span data-ttu-id="181dd-126">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="181dd-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181dd-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="181dd-127">-Confirm</span></span>
<span data-ttu-id="181dd-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="181dd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="181dd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="181dd-129">-WhatIf</span></span>
<span data-ttu-id="181dd-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="181dd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="181dd-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="181dd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="181dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181dd-132">CommonParameters</span></span>
<span data-ttu-id="181dd-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="181dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181dd-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="181dd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181dd-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="181dd-135">INPUTS</span></span>

## <span data-ttu-id="181dd-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="181dd-136">OUTPUTS</span></span>

### <span data-ttu-id="181dd-137">Microsoft. Azure. PowerShell. cmdlet. zaman</span><span class="sxs-lookup"><span data-stu-id="181dd-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="181dd-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="181dd-138">NOTES</span></span>

<span data-ttu-id="181dd-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="181dd-139">ALIASES</span></span>

## <span data-ttu-id="181dd-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="181dd-140">RELATED LINKS</span></span>

