---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 0dfbcabcb1869457e29d6c16c861c0743f50dc5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320030"
---
# <span data-ttu-id="0d816-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="0d816-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="0d816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d816-102">SYNOPSIS</span></span>
<span data-ttu-id="0d816-103">ApplicationGroup oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0d816-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="0d816-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d816-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d816-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d816-105">DESCRIPTION</span></span>
<span data-ttu-id="0d816-106">ApplicationGroup oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0d816-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="0d816-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d816-107">EXAMPLES</span></span>

### <span data-ttu-id="0d816-108">Örnek 1: ada göre bir Windows sanal masaüstü ApplicationGroup oluşturma</span><span class="sxs-lookup"><span data-stu-id="0d816-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="0d816-109">Bu komut, kaynak grubunda Windows sanal masaüstü ApplicationGroup grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0d816-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="0d816-110">Örnek 2: ada göre bir Windows sanal masaüstü ApplicationGroup oluşturma</span><span class="sxs-lookup"><span data-stu-id="0d816-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="0d816-111">Bu komut, kaynak grubunda Windows sanal masaüstü ApplicationGroup grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0d816-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="0d816-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d816-112">PARAMETERS</span></span>

### <span data-ttu-id="0d816-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="0d816-113">-ApplicationGroupType</span></span>
<span data-ttu-id="0d816-114">ApplicationGroup 'un kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="0d816-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d816-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d816-115">-DefaultProfile</span></span>
<span data-ttu-id="0d816-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d816-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d816-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="0d816-117">-Description</span></span>
<span data-ttu-id="0d816-118">ApplicationGroup 'un açıklaması.</span><span class="sxs-lookup"><span data-stu-id="0d816-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="0d816-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0d816-119">-FriendlyName</span></span>
<span data-ttu-id="0d816-120">ApplicationGroup 'un kolay adı.</span><span class="sxs-lookup"><span data-stu-id="0d816-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="0d816-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="0d816-121">-HostPoolArmPath</span></span>
<span data-ttu-id="0d816-122">ApplicationGroup 'un HostPool ARM yolu.</span><span class="sxs-lookup"><span data-stu-id="0d816-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="0d816-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="0d816-123">-Location</span></span>
<span data-ttu-id="0d816-124">Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="0d816-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="0d816-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d816-125">-Name</span></span>
<span data-ttu-id="0d816-126">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0d816-126">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d816-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d816-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d816-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0d816-128">The name of the resource group.</span></span>
<span data-ttu-id="0d816-129">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0d816-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0d816-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0d816-130">-SubscriptionId</span></span>
<span data-ttu-id="0d816-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0d816-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0d816-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0d816-132">-Tag</span></span>
<span data-ttu-id="0d816-133">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="0d816-133">Resource tags.</span></span>

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

### <span data-ttu-id="0d816-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d816-134">-Confirm</span></span>
<span data-ttu-id="0d816-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d816-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d816-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d816-136">-WhatIf</span></span>
<span data-ttu-id="0d816-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d816-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d816-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d816-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d816-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d816-139">CommonParameters</span></span>
<span data-ttu-id="0d816-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d816-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d816-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0d816-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d816-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d816-142">INPUTS</span></span>

## <span data-ttu-id="0d816-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d816-143">OUTPUTS</span></span>

### <span data-ttu-id="0d816-144">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıapplicationgroup</span><span class="sxs-lookup"><span data-stu-id="0d816-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="0d816-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d816-145">NOTES</span></span>

<span data-ttu-id="0d816-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0d816-146">ALIASES</span></span>

## <span data-ttu-id="0d816-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d816-147">RELATED LINKS</span></span>

