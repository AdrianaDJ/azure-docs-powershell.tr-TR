---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: fbd71d03c6f82bcb785105d9d75e155e9f7ef498
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320017"
---
# <span data-ttu-id="ad7a8-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="ad7a8-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="ad7a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad7a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7a8-103">Çalışma alanı oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-103">Create or update a workspace.</span></span>

## <span data-ttu-id="ad7a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad7a8-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad7a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad7a8-105">DESCRIPTION</span></span>
<span data-ttu-id="ad7a8-106">Çalışma alanı oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-106">Create or update a workspace.</span></span>

## <span data-ttu-id="ad7a8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad7a8-107">EXAMPLES</span></span>

### <span data-ttu-id="ad7a8-108">Örnek 1: ada göre bir Windows sanal masaüstü çalışma</span><span class="sxs-lookup"><span data-stu-id="ad7a8-108">Example 1: Create a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="ad7a8-109">Bu komut, kaynak grubunda Windows sanal masaüstü çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="ad7a8-110">Örnek 2: ada göre bir Windows sanal masaüstü çalışma</span><span class="sxs-lookup"><span data-stu-id="ad7a8-110">Example 2: Create a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="ad7a8-111">Bu komut, kaynak grubunda Windows sanal masaüstü çalışma alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="ad7a8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad7a8-112">PARAMETERS</span></span>

### <span data-ttu-id="ad7a8-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="ad7a8-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="ad7a8-114">ApplicationGroup kaynak kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-114">List of applicationGroup resource Ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7a8-115">-DefaultProfile</span></span>
<span data-ttu-id="ad7a8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad7a8-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ad7a8-117">-Description</span></span>
<span data-ttu-id="ad7a8-118">Çalışma alanının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="ad7a8-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ad7a8-119">-FriendlyName</span></span>
<span data-ttu-id="ad7a8-120">Çalışma alanının kolay adı.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="ad7a8-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="ad7a8-121">-Location</span></span>
<span data-ttu-id="ad7a8-122">Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="ad7a8-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="ad7a8-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad7a8-123">-Name</span></span>
<span data-ttu-id="ad7a8-124">Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="ad7a8-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7a8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad7a8-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad7a8-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-126">The name of the resource group.</span></span>
<span data-ttu-id="ad7a8-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ad7a8-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ad7a8-128">-SubscriptionId</span></span>
<span data-ttu-id="ad7a8-129">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ad7a8-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ad7a8-130">-Tag</span></span>
<span data-ttu-id="ad7a8-131">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7a8-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad7a8-132">-Confirm</span></span>
<span data-ttu-id="ad7a8-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad7a8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad7a8-134">-WhatIf</span></span>
<span data-ttu-id="ad7a8-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad7a8-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad7a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7a8-137">CommonParameters</span></span>
<span data-ttu-id="ad7a8-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7a8-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ad7a8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7a8-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad7a8-140">INPUTS</span></span>

## <span data-ttu-id="ad7a8-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad7a8-141">OUTPUTS</span></span>

### <span data-ttu-id="ad7a8-142">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıworkspace</span><span class="sxs-lookup"><span data-stu-id="ad7a8-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="ad7a8-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad7a8-143">NOTES</span></span>

<span data-ttu-id="ad7a8-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ad7a8-144">ALIASES</span></span>

## <span data-ttu-id="ad7a8-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad7a8-145">RELATED LINKS</span></span>

