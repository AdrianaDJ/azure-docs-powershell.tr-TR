---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 1e4526d164e00e3b441889938e7d918634a93dc4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936357"
---
# <span data-ttu-id="fbdfe-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="fbdfe-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="fbdfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbdfe-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdfe-103">Yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="fbdfe-103">Removes a managed application definition</span></span>

## <span data-ttu-id="fbdfe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbdfe-104">SYNTAX</span></span>

### <span data-ttu-id="fbdfe-105">Removebynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fbdfe-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbdfe-106">Removebyıd</span><span class="sxs-lookup"><span data-stu-id="fbdfe-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbdfe-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbdfe-107">DESCRIPTION</span></span>
<span data-ttu-id="fbdfe-108">**Remove-AzManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="fbdfe-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="fbdfe-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbdfe-109">EXAMPLES</span></span>

### <span data-ttu-id="fbdfe-110">Örnek 1: yönetilen uygulama tanımını kaynak KIMLIĞIYLE kaldırma</span><span class="sxs-lookup"><span data-stu-id="fbdfe-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="fbdfe-111">İlk komut, Get-AzManagedApplicationDefinition cmdlet 'ini kullanarak myAppDef adlı bir yönetilen uygulama tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="fbdfe-112">Komut, $ApplicationDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="fbdfe-113">İkinci komut, $ApplicationDefinition 'in **RESOURCEID** özelliğiyle tanımlanan yönetilen uygulama tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="fbdfe-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbdfe-114">PARAMETERS</span></span>

### <span data-ttu-id="fbdfe-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="fbdfe-115">-ApiVersion</span></span>
<span data-ttu-id="fbdfe-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fbdfe-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fbdfe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdfe-118">-DefaultProfile</span></span>
<span data-ttu-id="fbdfe-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdfe-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fbdfe-120">-Force</span></span>
<span data-ttu-id="fbdfe-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fbdfe-122">-ID</span><span class="sxs-lookup"><span data-stu-id="fbdfe-122">-Id</span></span>
<span data-ttu-id="fbdfe-123">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="fbdfe-124">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="fbdfe-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="fbdfe-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="fbdfe-125">-Name</span></span>
<span data-ttu-id="fbdfe-126">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="fbdfe-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="fbdfe-127">-Pre</span></span>
<span data-ttu-id="fbdfe-128">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fbdfe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbdfe-129">-ResourceGroupName</span></span>
<span data-ttu-id="fbdfe-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-130">The resource group name.</span></span>

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

### <span data-ttu-id="fbdfe-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbdfe-131">-Confirm</span></span>
<span data-ttu-id="fbdfe-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbdfe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbdfe-133">-WhatIf</span></span>
<span data-ttu-id="fbdfe-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbdfe-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbdfe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdfe-136">CommonParameters</span></span>
<span data-ttu-id="fbdfe-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbdfe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdfe-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbdfe-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdfe-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbdfe-139">INPUTS</span></span>

### <span data-ttu-id="fbdfe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fbdfe-140">System.String</span></span>

## <span data-ttu-id="fbdfe-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbdfe-141">OUTPUTS</span></span>

### <span data-ttu-id="fbdfe-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fbdfe-142">System.Boolean</span></span>

## <span data-ttu-id="fbdfe-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbdfe-143">NOTES</span></span>

## <span data-ttu-id="fbdfe-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbdfe-144">RELATED LINKS</span></span>
