---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274291"
---
# <span data-ttu-id="f2755-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="f2755-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="f2755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2755-102">SYNOPSIS</span></span>
<span data-ttu-id="f2755-103">Panoyu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f2755-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="f2755-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2755-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2755-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2755-105">DESCRIPTION</span></span>
<span data-ttu-id="f2755-106">Panoyu oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f2755-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="f2755-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2755-107">EXAMPLES</span></span>

### <span data-ttu-id="f2755-108">Örnek 1: Pano şablonunu kullanarak Pano tanımını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f2755-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="f2755-109">Bir pano tanımını, bir çizgi temelşablonu dosyası kullanarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f2755-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="f2755-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2755-110">PARAMETERS</span></span>

### <span data-ttu-id="f2755-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="f2755-111">-DashboardPath</span></span>
<span data-ttu-id="f2755-112">Var olan pano şablonunun yolu.</span><span class="sxs-lookup"><span data-stu-id="f2755-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="f2755-113">Pano şablonları portaldan indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f2755-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="f2755-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2755-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="f2755-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2755-115">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2755-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2755-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="f2755-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f2755-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="f2755-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2755-118">-Confirm</span></span>
<span data-ttu-id="f2755-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2755-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2755-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2755-120">-WhatIf</span></span>
<span data-ttu-id="f2755-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2755-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2755-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2755-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2755-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2755-123">CommonParameters</span></span>
<span data-ttu-id="f2755-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2755-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2755-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f2755-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2755-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2755-126">INPUTS</span></span>

## <span data-ttu-id="f2755-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2755-127">OUTPUTS</span></span>

### <span data-ttu-id="f2755-128">Microsoft. Azure. PowerShell. cmdlet. Portal. modeller. Api201901Preview. ıdashboard</span><span class="sxs-lookup"><span data-stu-id="f2755-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="f2755-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2755-129">NOTES</span></span>

<span data-ttu-id="f2755-130">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f2755-130">ALIASES</span></span>

## <span data-ttu-id="f2755-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2755-131">RELATED LINKS</span></span>

