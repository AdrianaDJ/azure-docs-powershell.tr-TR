---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322699"
---
# <span data-ttu-id="97990-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97990-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="97990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97990-102">SYNOPSIS</span></span>
<span data-ttu-id="97990-103">Application Insights bağlantılı depolama hesabını alma</span><span class="sxs-lookup"><span data-stu-id="97990-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="97990-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97990-104">SYNTAX</span></span>

### <span data-ttu-id="97990-105">ByResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97990-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97990-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97990-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97990-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="97990-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97990-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="97990-108">DESCRIPTION</span></span>
<span data-ttu-id="97990-109">Application Insights bağlantılı depolama hesabını alma</span><span class="sxs-lookup"><span data-stu-id="97990-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="97990-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97990-110">EXAMPLES</span></span>

### <span data-ttu-id="97990-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="97990-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="97990-112">"ComponentName" bileşeniyle ilişkilendirilmiş bağlantılı depolama hesabını al</span><span class="sxs-lookup"><span data-stu-id="97990-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="97990-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97990-113">PARAMETERS</span></span>

### <span data-ttu-id="97990-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="97990-114">-ComponentName</span></span>
<span data-ttu-id="97990-115">Bileşen adı</span><span class="sxs-lookup"><span data-stu-id="97990-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97990-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97990-116">-DefaultProfile</span></span>
<span data-ttu-id="97990-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97990-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97990-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97990-118">-InputObject</span></span>
<span data-ttu-id="97990-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="97990-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97990-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97990-120">-ResourceGroupName</span></span>
<span data-ttu-id="97990-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="97990-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97990-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97990-122">-ResourceId</span></span>
<span data-ttu-id="97990-123">Bileşen RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97990-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97990-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97990-124">CommonParameters</span></span>
<span data-ttu-id="97990-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97990-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97990-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="97990-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97990-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97990-127">INPUTS</span></span>

### <span data-ttu-id="97990-128">System. String</span><span class="sxs-lookup"><span data-stu-id="97990-128">System.String</span></span>

### <span data-ttu-id="97990-129">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="97990-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="97990-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97990-130">OUTPUTS</span></span>

### <span data-ttu-id="97990-131">Microsoft. Azure. Commands. ApplicationInsights. model. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="97990-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="97990-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97990-132">NOTES</span></span>

## <span data-ttu-id="97990-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97990-133">RELATED LINKS</span></span>
