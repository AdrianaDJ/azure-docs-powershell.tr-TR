---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 77cefc15467cc5fc553761457889aaf2ca770704
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932551"
---
# <span data-ttu-id="1c11b-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="1c11b-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="1c11b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c11b-102">SYNOPSIS</span></span>
<span data-ttu-id="1c11b-103">Yönetilen uygulamayı kaldırır</span><span class="sxs-lookup"><span data-stu-id="1c11b-103">Removes a managed application</span></span>

## <span data-ttu-id="1c11b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c11b-104">SYNTAX</span></span>

### <span data-ttu-id="1c11b-105">Removebynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1c11b-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c11b-106">Removebyıd</span><span class="sxs-lookup"><span data-stu-id="1c11b-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c11b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c11b-107">DESCRIPTION</span></span>
<span data-ttu-id="1c11b-108">**Remove-AzManagedApplication** cmdlet 'i yönetilen uygulamayı kaldırır</span><span class="sxs-lookup"><span data-stu-id="1c11b-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="1c11b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c11b-109">EXAMPLES</span></span>

### <span data-ttu-id="1c11b-110">Örnek 1: yönetilen uygulamayı kaynak KIMLIĞIYLE kaldırma</span><span class="sxs-lookup"><span data-stu-id="1c11b-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="1c11b-111">İlk komut, Uygulamam adlı bir yönetilen uygulamayı Get-AzManagedApplication cmdlet 'i kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="1c11b-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="1c11b-112">Komut, $Application değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1c11b-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="1c11b-113">İkinci komut $Application 'in **RESOURCEID** özelliğiyle tanımlanan yönetilen uygulamayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1c11b-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="1c11b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c11b-114">PARAMETERS</span></span>

### <span data-ttu-id="1c11b-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="1c11b-115">-ApiVersion</span></span>
<span data-ttu-id="1c11b-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c11b-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1c11b-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1c11b-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1c11b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c11b-118">-DefaultProfile</span></span>
<span data-ttu-id="1c11b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c11b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c11b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1c11b-120">-Force</span></span>
<span data-ttu-id="1c11b-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="1c11b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1c11b-122">-ID</span><span class="sxs-lookup"><span data-stu-id="1c11b-122">-Id</span></span>
<span data-ttu-id="1c11b-123">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="1c11b-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="1c11b-124">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="1c11b-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c11b-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="1c11b-125">-Name</span></span>
<span data-ttu-id="1c11b-126">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="1c11b-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c11b-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="1c11b-127">-Pre</span></span>
<span data-ttu-id="1c11b-128">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c11b-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1c11b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c11b-129">-ResourceGroupName</span></span>
<span data-ttu-id="1c11b-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1c11b-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c11b-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c11b-131">-Confirm</span></span>
<span data-ttu-id="1c11b-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c11b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c11b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c11b-133">-WhatIf</span></span>
<span data-ttu-id="1c11b-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c11b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c11b-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c11b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c11b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c11b-136">CommonParameters</span></span>
<span data-ttu-id="1c11b-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c11b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c11b-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c11b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c11b-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c11b-139">INPUTS</span></span>

### <span data-ttu-id="1c11b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1c11b-140">System.String</span></span>

## <span data-ttu-id="1c11b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c11b-141">OUTPUTS</span></span>

### <span data-ttu-id="1c11b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c11b-142">System.Boolean</span></span>

## <span data-ttu-id="1c11b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c11b-143">NOTES</span></span>

## <span data-ttu-id="1c11b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c11b-144">RELATED LINKS</span></span>
