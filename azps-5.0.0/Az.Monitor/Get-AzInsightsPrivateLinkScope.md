---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278599"
---
# <span data-ttu-id="d4125-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d4125-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="d4125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4125-102">SYNOPSIS</span></span>
<span data-ttu-id="d4125-103">Özel bağlantı kapsamını alma</span><span class="sxs-lookup"><span data-stu-id="d4125-103">Get private link scope</span></span>

## <span data-ttu-id="d4125-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4125-104">SYNTAX</span></span>

### <span data-ttu-id="d4125-105">ByResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4125-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4125-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4125-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4125-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d4125-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4125-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4125-108">DESCRIPTION</span></span>
<span data-ttu-id="d4125-109">Özel bağlantı kapsamını listeler veya alın</span><span class="sxs-lookup"><span data-stu-id="d4125-109">List or get private link scope</span></span> 

## <span data-ttu-id="d4125-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4125-110">EXAMPLES</span></span>

### <span data-ttu-id="d4125-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d4125-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="d4125-112">"Rg_name" kaynak grubu altındaki özel bağlantı kapsamlarını listeler</span><span class="sxs-lookup"><span data-stu-id="d4125-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="d4125-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d4125-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="d4125-114">"Rg_name" kaynak grubu altındaki "scope_name" adlı özel bağlantı kapsamını alma</span><span class="sxs-lookup"><span data-stu-id="d4125-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="d4125-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4125-115">PARAMETERS</span></span>

### <span data-ttu-id="d4125-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4125-116">-DefaultProfile</span></span>
<span data-ttu-id="d4125-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4125-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4125-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4125-118">-Name</span></span>
<span data-ttu-id="d4125-119">Özel bağlantı kapsamı adı</span><span class="sxs-lookup"><span data-stu-id="d4125-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="d4125-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4125-120">-ResourceGroupName</span></span>
<span data-ttu-id="d4125-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d4125-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="d4125-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d4125-122">-ResourceId</span></span>
<span data-ttu-id="d4125-123">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d4125-123">Resource Id</span></span>

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

### <span data-ttu-id="d4125-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4125-124">CommonParameters</span></span>
<span data-ttu-id="d4125-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4125-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4125-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d4125-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4125-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4125-127">INPUTS</span></span>

### <span data-ttu-id="d4125-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d4125-128">System.String</span></span>

## <span data-ttu-id="d4125-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4125-129">OUTPUTS</span></span>

### <span data-ttu-id="d4125-130">Microsoft. Azure. Commands. Insights. OutputClasses. Psmte ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="d4125-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="d4125-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4125-131">NOTES</span></span>

## <span data-ttu-id="d4125-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4125-132">RELATED LINKS</span></span>
