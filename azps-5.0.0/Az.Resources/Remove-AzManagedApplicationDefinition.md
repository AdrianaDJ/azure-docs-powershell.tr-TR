---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322831"
---
# <span data-ttu-id="74c7c-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="74c7c-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="74c7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="74c7c-103">Yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="74c7c-103">Removes a managed application definition</span></span>

## <span data-ttu-id="74c7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74c7c-104">SYNTAX</span></span>

### <span data-ttu-id="74c7c-105">Removebynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="74c7c-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74c7c-106">Removebyıd</span><span class="sxs-lookup"><span data-stu-id="74c7c-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74c7c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="74c7c-107">DESCRIPTION</span></span>
<span data-ttu-id="74c7c-108">**Remove-AzManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="74c7c-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="74c7c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74c7c-109">EXAMPLES</span></span>

### <span data-ttu-id="74c7c-110">Örnek 1: yönetilen uygulama tanımını kaynak KIMLIĞIYLE kaldırma</span><span class="sxs-lookup"><span data-stu-id="74c7c-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="74c7c-111">İlk komut, Get-AzManagedApplicationDefinition cmdlet 'ini kullanarak myAppDef adlı bir yönetilen uygulama tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="74c7c-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="74c7c-112">Komut, $ApplicationDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="74c7c-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="74c7c-113">İkinci komut, $ApplicationDefinition 'in **RESOURCEID** özelliğiyle tanımlanan yönetilen uygulama tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="74c7c-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="74c7c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74c7c-114">PARAMETERS</span></span>

### <span data-ttu-id="74c7c-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="74c7c-115">-ApiVersion</span></span>
<span data-ttu-id="74c7c-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="74c7c-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="74c7c-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="74c7c-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="74c7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c7c-118">-DefaultProfile</span></span>
<span data-ttu-id="74c7c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74c7c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74c7c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="74c7c-120">-Force</span></span>
<span data-ttu-id="74c7c-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="74c7c-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="74c7c-122">-ID</span><span class="sxs-lookup"><span data-stu-id="74c7c-122">-Id</span></span>
<span data-ttu-id="74c7c-123">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="74c7c-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="74c7c-124">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="74c7c-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="74c7c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="74c7c-125">-Name</span></span>
<span data-ttu-id="74c7c-126">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="74c7c-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="74c7c-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="74c7c-127">-Pre</span></span>
<span data-ttu-id="74c7c-128">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74c7c-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="74c7c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c7c-129">-ResourceGroupName</span></span>
<span data-ttu-id="74c7c-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="74c7c-130">The resource group name.</span></span>

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

### <span data-ttu-id="74c7c-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="74c7c-131">-Confirm</span></span>
<span data-ttu-id="74c7c-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74c7c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c7c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c7c-133">-WhatIf</span></span>
<span data-ttu-id="74c7c-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74c7c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c7c-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74c7c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c7c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c7c-136">CommonParameters</span></span>
<span data-ttu-id="74c7c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74c7c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c7c-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="74c7c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c7c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74c7c-139">INPUTS</span></span>

### <span data-ttu-id="74c7c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="74c7c-140">System.String</span></span>

## <span data-ttu-id="74c7c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74c7c-141">OUTPUTS</span></span>

### <span data-ttu-id="74c7c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74c7c-142">System.Boolean</span></span>

## <span data-ttu-id="74c7c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74c7c-143">NOTES</span></span>

## <span data-ttu-id="74c7c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74c7c-144">RELATED LINKS</span></span>
