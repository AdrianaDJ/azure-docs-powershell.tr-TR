---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268137"
---
# <span data-ttu-id="d24a6-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d24a6-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="d24a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d24a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d24a6-103">var olan Application Insights kaynağını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d24a6-103">update an existing application insights resource</span></span>

## <span data-ttu-id="d24a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d24a6-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d24a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d24a6-105">DESCRIPTION</span></span>
<span data-ttu-id="d24a6-106">var olan Application Insights kaynağını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d24a6-106">update an existing application insights resource</span></span>

## <span data-ttu-id="d24a6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d24a6-107">EXAMPLES</span></span>

### <span data-ttu-id="d24a6-108">Örnek 1 Application Insights bileşenini Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="d24a6-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="d24a6-109">Application Insights bileşenini "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery ile birlikte "Disabled" olarak güncelleyin</span><span class="sxs-lookup"><span data-stu-id="d24a6-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="d24a6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d24a6-110">PARAMETERS</span></span>

### <span data-ttu-id="d24a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24a6-111">-DefaultProfile</span></span>
<span data-ttu-id="d24a6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d24a6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24a6-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d24a6-113">-Name</span></span>
<span data-ttu-id="d24a6-114">Application Insights kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d24a6-114">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24a6-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="d24a6-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="d24a6-116">Uygulama öngörülerini uygulamaya erişmek için ağ erişim türü.</span><span class="sxs-lookup"><span data-stu-id="d24a6-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="d24a6-117">Değer ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="d24a6-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24a6-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="d24a6-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="d24a6-119">Application Insights sorgusuna erişmek için ağ erişim türü.</span><span class="sxs-lookup"><span data-stu-id="d24a6-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="d24a6-120">Değer ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="d24a6-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24a6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24a6-121">-ResourceGroupName</span></span>
<span data-ttu-id="d24a6-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d24a6-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24a6-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d24a6-123">-RetentionInDays</span></span>
<span data-ttu-id="d24a6-124">Gün Içinde 90 varsayılan olarak.</span><span class="sxs-lookup"><span data-stu-id="d24a6-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24a6-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d24a6-125">-Tag</span></span>
<span data-ttu-id="d24a6-126">Bileşen etiketleri.</span><span class="sxs-lookup"><span data-stu-id="d24a6-126">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24a6-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="d24a6-127">-Confirm</span></span>
<span data-ttu-id="d24a6-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d24a6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d24a6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d24a6-129">-WhatIf</span></span>
<span data-ttu-id="d24a6-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d24a6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d24a6-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d24a6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d24a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24a6-132">CommonParameters</span></span>
<span data-ttu-id="d24a6-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d24a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24a6-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d24a6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24a6-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d24a6-135">INPUTS</span></span>

### <span data-ttu-id="d24a6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d24a6-136">System.String</span></span>

## <span data-ttu-id="d24a6-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d24a6-137">OUTPUTS</span></span>

### <span data-ttu-id="d24a6-138">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d24a6-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="d24a6-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d24a6-139">NOTES</span></span>

## <span data-ttu-id="d24a6-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d24a6-140">RELATED LINKS</span></span>
