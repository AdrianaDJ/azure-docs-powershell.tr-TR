---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: b91332fe8867283b5fff9cbbf1f5df96209fa2f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107791"
---
# <span data-ttu-id="c11e8-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="c11e8-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="c11e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c11e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c11e8-103">Konak havuzu oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c11e8-103">Create or update a host pool.</span></span>

## <span data-ttu-id="c11e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c11e8-104">SYNTAX</span></span>

### <span data-ttu-id="c11e8-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c11e8-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoContext <String>]
 [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c11e8-106">Tamseneriocreate</span><span class="sxs-lookup"><span data-stu-id="c11e8-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c11e8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c11e8-107">DESCRIPTION</span></span>
<span data-ttu-id="c11e8-108">Konak havuzu oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c11e8-108">Create or update a host pool.</span></span>

## <span data-ttu-id="c11e8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c11e8-109">EXAMPLES</span></span>

### <span data-ttu-id="c11e8-110">Örnek 1: ada göre bir Windows sanal masaüstü HostPool oluşturma</span><span class="sxs-lookup"><span data-stu-id="c11e8-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="c11e8-111">Bu komut, kaynak grubunda Windows sanal masaüstü HostPool oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c11e8-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="c11e8-112">Örnek 1: ada göre bir Windows sanal masaüstü HostPool oluşturma</span><span class="sxs-lookup"><span data-stu-id="c11e8-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="c11e8-113">Bu komut, kaynak grubunda Windows sanal masaüstü HostPool oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c11e8-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="c11e8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c11e8-114">PARAMETERS</span></span>

### <span data-ttu-id="c11e8-115">-Customrdpözelliği</span><span class="sxs-lookup"><span data-stu-id="c11e8-115">-CustomRdpProperty</span></span>
<span data-ttu-id="c11e8-116">HostPool 'un özel RDP özelliği.</span><span class="sxs-lookup"><span data-stu-id="c11e8-116">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11e8-117">-DefaultProfile</span></span>
<span data-ttu-id="c11e8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c11e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c11e8-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c11e8-119">-Description</span></span>
<span data-ttu-id="c11e8-120">Anabilgisayarhavuzunun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="c11e8-120">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="c11e8-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="c11e8-122">Masaüstü uygulama grubu adı</span><span class="sxs-lookup"><span data-stu-id="c11e8-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="c11e8-123">-ExpirationTime</span></span>
<span data-ttu-id="c11e8-124">Kayıt belirtecinin son kullanma tarihi.</span><span class="sxs-lookup"><span data-stu-id="c11e8-124">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c11e8-125">-FriendlyName</span></span>
<span data-ttu-id="c11e8-126">HostPool kolay adı.</span><span class="sxs-lookup"><span data-stu-id="c11e8-126">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="c11e8-127">-HostPoolType</span></span>
<span data-ttu-id="c11e8-128">Masaüstü için Anabilgisayarhavuz türü.</span><span class="sxs-lookup"><span data-stu-id="c11e8-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="c11e8-129">-LoadBalancerType</span></span>
<span data-ttu-id="c11e8-130">Yük dengeleyicinin türü.</span><span class="sxs-lookup"><span data-stu-id="c11e8-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="c11e8-131">-Location</span></span>
<span data-ttu-id="c11e8-132">Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="c11e8-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="c11e8-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="c11e8-133">-MaxSessionLimit</span></span>
<span data-ttu-id="c11e8-134">HostPool için en fazla oturum sınırı.</span><span class="sxs-lookup"><span data-stu-id="c11e8-134">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="c11e8-135">-Name</span></span>
<span data-ttu-id="c11e8-136">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="c11e8-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-137">-Persondesktopassignmenttype</span><span class="sxs-lookup"><span data-stu-id="c11e8-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="c11e8-138">PersonalDesktopAssignment türü.</span><span class="sxs-lookup"><span data-stu-id="c11e8-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="c11e8-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="c11e8-140">Tercih edilen uygulama grubu türünün türü, varsayılan masaüstü uygulama grubu</span><span class="sxs-lookup"><span data-stu-id="c11e8-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-141">-Registrationınfotoken</span><span class="sxs-lookup"><span data-stu-id="c11e8-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="c11e8-142">Kayıt belirteci base64 kodlamalı dizesi.</span><span class="sxs-lookup"><span data-stu-id="c11e8-142">The registration token base64 encoded string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="c11e8-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="c11e8-144">Belirteci sıfırlama türü.</span><span class="sxs-lookup"><span data-stu-id="c11e8-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c11e8-145">-ResourceGroupName</span></span>
<span data-ttu-id="c11e8-146">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c11e8-146">The name of the resource group.</span></span>
<span data-ttu-id="c11e8-147">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="c11e8-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c11e8-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="c11e8-148">-Ring</span></span>
<span data-ttu-id="c11e8-149">Anabilgisayarhavuzunun zil sesi numarası.</span><span class="sxs-lookup"><span data-stu-id="c11e8-149">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-150">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="c11e8-150">-SsoContext</span></span>
<span data-ttu-id="c11e8-151">SsoContext Secret içeren tuş Kasası yolu.</span><span class="sxs-lookup"><span data-stu-id="c11e8-151">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-152">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c11e8-152">-SubscriptionId</span></span>
<span data-ttu-id="c11e8-153">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c11e8-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c11e8-154">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c11e8-154">-Tag</span></span>
<span data-ttu-id="c11e8-155">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="c11e8-155">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="c11e8-156">-ValidationEnvironment</span></span>
<span data-ttu-id="c11e8-157">Doğrulama ortamıdır.</span><span class="sxs-lookup"><span data-stu-id="c11e8-157">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="c11e8-158">-VMTemplate</span></span>
<span data-ttu-id="c11e8-159">Hostpool içinde sessionhosts yapılandırması için VM şablonu.</span><span class="sxs-lookup"><span data-stu-id="c11e8-159">VM template for sessionhosts configuration within hostpool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-160">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="c11e8-160">-WorkspaceName</span></span>
<span data-ttu-id="c11e8-161">Çalışma alanı adı</span><span class="sxs-lookup"><span data-stu-id="c11e8-161">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11e8-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="c11e8-162">-Confirm</span></span>
<span data-ttu-id="c11e8-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c11e8-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c11e8-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c11e8-164">-WhatIf</span></span>
<span data-ttu-id="c11e8-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c11e8-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c11e8-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c11e8-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c11e8-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11e8-167">CommonParameters</span></span>
<span data-ttu-id="c11e8-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c11e8-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11e8-169">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c11e8-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11e8-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c11e8-170">INPUTS</span></span>

## <span data-ttu-id="c11e8-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c11e8-171">OUTPUTS</span></span>

### <span data-ttu-id="c11e8-172">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıhostpool</span><span class="sxs-lookup"><span data-stu-id="c11e8-172">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="c11e8-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c11e8-173">NOTES</span></span>

<span data-ttu-id="c11e8-174">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c11e8-174">ALIASES</span></span>

## <span data-ttu-id="c11e8-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c11e8-175">RELATED LINKS</span></span>

