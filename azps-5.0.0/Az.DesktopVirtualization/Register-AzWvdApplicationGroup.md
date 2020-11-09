---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320006"
---
# <span data-ttu-id="edc8e-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="edc8e-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="edc8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edc8e-102">SYNOPSIS</span></span>
<span data-ttu-id="edc8e-103">Windows sanal masaüstü uygulama grubunu kaydettirme.</span><span class="sxs-lookup"><span data-stu-id="edc8e-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="edc8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edc8e-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="edc8e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edc8e-105">DESCRIPTION</span></span>
<span data-ttu-id="edc8e-106">Windows sanal masaüstü uygulama grubunu kaydettirme.</span><span class="sxs-lookup"><span data-stu-id="edc8e-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="edc8e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edc8e-107">EXAMPLES</span></span>

### <span data-ttu-id="edc8e-108">Örnek 1: Windows sanal masaüstü uygulaması grubunu kaydettirme</span><span class="sxs-lookup"><span data-stu-id="edc8e-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="edc8e-109">Bu komut bir Windows sanal masaüstü uygulama grubunu çalışma alanına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="edc8e-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="edc8e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edc8e-110">PARAMETERS</span></span>

### <span data-ttu-id="edc8e-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="edc8e-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="edc8e-112">ApplicationGroupPath yolu</span><span class="sxs-lookup"><span data-stu-id="edc8e-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="edc8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc8e-113">-DefaultProfile</span></span>
<span data-ttu-id="edc8e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edc8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edc8e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc8e-115">-ResourceGroupName</span></span>
<span data-ttu-id="edc8e-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="edc8e-116">Resource Group Name</span></span>

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

### <span data-ttu-id="edc8e-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="edc8e-117">-SubscriptionId</span></span>
<span data-ttu-id="edc8e-118">Abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="edc8e-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc8e-119">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="edc8e-119">-WorkspaceName</span></span>
<span data-ttu-id="edc8e-120">Çalışma alanı adı</span><span class="sxs-lookup"><span data-stu-id="edc8e-120">Workspace Name</span></span>

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

### <span data-ttu-id="edc8e-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="edc8e-121">-Confirm</span></span>
<span data-ttu-id="edc8e-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edc8e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edc8e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc8e-123">-WhatIf</span></span>
<span data-ttu-id="edc8e-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edc8e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edc8e-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edc8e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edc8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc8e-126">CommonParameters</span></span>
<span data-ttu-id="edc8e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edc8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc8e-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="edc8e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc8e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edc8e-129">INPUTS</span></span>

## <span data-ttu-id="edc8e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edc8e-130">OUTPUTS</span></span>

### <span data-ttu-id="edc8e-131">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıworkspace</span><span class="sxs-lookup"><span data-stu-id="edc8e-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="edc8e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edc8e-132">NOTES</span></span>

<span data-ttu-id="edc8e-133">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="edc8e-133">ALIASES</span></span>

## <span data-ttu-id="edc8e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edc8e-134">RELATED LINKS</span></span>

