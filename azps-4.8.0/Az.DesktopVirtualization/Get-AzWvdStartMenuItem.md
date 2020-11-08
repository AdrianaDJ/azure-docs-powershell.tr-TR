---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: d4390f7de7b9fb91cf998050f192a3ba282e9585
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268271"
---
# <span data-ttu-id="46f71-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="46f71-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="46f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f71-102">SYNOPSIS</span></span>
<span data-ttu-id="46f71-103">Verilen uygulama grubundaki başlangıç menüsü öğelerini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="46f71-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="46f71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46f71-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="46f71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46f71-105">DESCRIPTION</span></span>
<span data-ttu-id="46f71-106">Verilen uygulama grubundaki başlangıç menüsü öğelerini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="46f71-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="46f71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46f71-107">EXAMPLES</span></span>

### <span data-ttu-id="46f71-108">Örnek 2: Windows sanal masaüstü Başlat menüsü öğelerini listele</span><span class="sxs-lookup"><span data-stu-id="46f71-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="46f71-109">Bu komut, bir grup grubundaki Windows sanal masaüstü Başlat menüsü öğelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="46f71-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="46f71-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46f71-110">PARAMETERS</span></span>

### <span data-ttu-id="46f71-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="46f71-111">-ApplicationGroupName</span></span>
<span data-ttu-id="46f71-112">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="46f71-112">The name of the application group</span></span>

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

### <span data-ttu-id="46f71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f71-113">-DefaultProfile</span></span>
<span data-ttu-id="46f71-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46f71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46f71-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f71-115">-ResourceGroupName</span></span>
<span data-ttu-id="46f71-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="46f71-116">The name of the resource group.</span></span>
<span data-ttu-id="46f71-117">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="46f71-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="46f71-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="46f71-118">-SubscriptionId</span></span>
<span data-ttu-id="46f71-119">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="46f71-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f71-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f71-120">CommonParameters</span></span>
<span data-ttu-id="46f71-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46f71-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f71-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46f71-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f71-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46f71-123">INPUTS</span></span>

## <span data-ttu-id="46f71-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46f71-124">OUTPUTS</span></span>

### <span data-ttu-id="46f71-125">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. Istartmenuıtem</span><span class="sxs-lookup"><span data-stu-id="46f71-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IStartMenuItem</span></span>

## <span data-ttu-id="46f71-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46f71-126">NOTES</span></span>

<span data-ttu-id="46f71-127">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="46f71-127">ALIASES</span></span>

## <span data-ttu-id="46f71-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46f71-128">RELATED LINKS</span></span>

