---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324853"
---
# <span data-ttu-id="e477e-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="e477e-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="e477e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e477e-102">SYNOPSIS</span></span>
<span data-ttu-id="e477e-103">Özel bulutta ExpressRoute devresi yetkilendirmesi oluşturma veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e477e-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="e477e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e477e-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e477e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e477e-105">DESCRIPTION</span></span>
<span data-ttu-id="e477e-106">Özel bulutta ExpressRoute devresi yetkilendirmesi oluşturma veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e477e-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="e477e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e477e-107">EXAMPLES</span></span>

### <span data-ttu-id="e477e-108">Örnek 1: oluşturma Autorization</span><span class="sxs-lookup"><span data-stu-id="e477e-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="e477e-109">Bu cmdlet `azps-test-auth` özel bulut altında yetkilendirme oluşturur `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="e477e-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="e477e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e477e-110">PARAMETERS</span></span>

### <span data-ttu-id="e477e-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="e477e-111">-AsJob</span></span>
<span data-ttu-id="e477e-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="e477e-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e477e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e477e-113">-DefaultProfile</span></span>
<span data-ttu-id="e477e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e477e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e477e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e477e-115">-Name</span></span>
<span data-ttu-id="e477e-116">Özel bulutta ExpressRoute devresi yetkilendirmesi adı</span><span class="sxs-lookup"><span data-stu-id="e477e-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e477e-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e477e-117">-NoWait</span></span>
<span data-ttu-id="e477e-118">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="e477e-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e477e-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="e477e-119">-PrivateCloudName</span></span>
<span data-ttu-id="e477e-120">Özel bulutun adı.</span><span class="sxs-lookup"><span data-stu-id="e477e-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="e477e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e477e-121">-ResourceGroupName</span></span>
<span data-ttu-id="e477e-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e477e-122">The name of the resource group.</span></span>
<span data-ttu-id="e477e-123">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="e477e-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e477e-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e477e-124">-SubscriptionId</span></span>
<span data-ttu-id="e477e-125">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e477e-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e477e-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="e477e-126">-Confirm</span></span>
<span data-ttu-id="e477e-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e477e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e477e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e477e-128">-WhatIf</span></span>
<span data-ttu-id="e477e-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e477e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e477e-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e477e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e477e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e477e-131">CommonParameters</span></span>
<span data-ttu-id="e477e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e477e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e477e-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e477e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e477e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e477e-134">INPUTS</span></span>

## <span data-ttu-id="e477e-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e477e-135">OUTPUTS</span></span>

### <span data-ttu-id="e477e-136">Microsoft. Azure. PowerShell. cmdlet. VMWare. modeller. Api20200320. ıexpressrouteauthorization</span><span class="sxs-lookup"><span data-stu-id="e477e-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="e477e-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e477e-137">NOTES</span></span>

<span data-ttu-id="e477e-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="e477e-138">ALIASES</span></span>

## <span data-ttu-id="e477e-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e477e-139">RELATED LINKS</span></span>

