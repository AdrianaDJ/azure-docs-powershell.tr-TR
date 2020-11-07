---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: 41cf22aab3cc79499d5a2c8918197c1cd6d092e6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940006"
---
# <span data-ttu-id="371ab-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="371ab-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="371ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="371ab-102">SYNOPSIS</span></span>
<span data-ttu-id="371ab-103">Yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="371ab-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="371ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="371ab-104">SYNTAX</span></span>

### <span data-ttu-id="371ab-105">Removebynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="371ab-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="371ab-106">Removebyıd</span><span class="sxs-lookup"><span data-stu-id="371ab-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="371ab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="371ab-107">DESCRIPTION</span></span>
<span data-ttu-id="371ab-108">**Remove-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="371ab-108">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="371ab-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="371ab-109">EXAMPLES</span></span>

### <span data-ttu-id="371ab-110">Örnek 1: yönetilen uygulama tanımını kaynak KIMLIĞIYLE kaldırma</span><span class="sxs-lookup"><span data-stu-id="371ab-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="371ab-111">İlk komut, Get-AzureRmManagedApplicationDefinition cmdlet 'ini kullanarak myAppDef adlı bir yönetilen uygulama tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="371ab-111">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="371ab-112">Komut, $ApplicationDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="371ab-112">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="371ab-113">İkinci komut, $ApplicationDefinition 'in **RESOURCEID** özelliğiyle tanımlanan yönetilen uygulama tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="371ab-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="371ab-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="371ab-114">PARAMETERS</span></span>

### <span data-ttu-id="371ab-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="371ab-115">-ApiVersion</span></span>
<span data-ttu-id="371ab-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="371ab-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="371ab-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="371ab-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="371ab-118">-DefaultProfile</span></span>
<span data-ttu-id="371ab-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="371ab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371ab-120">-Force</span><span class="sxs-lookup"><span data-stu-id="371ab-120">-Force</span></span>
<span data-ttu-id="371ab-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="371ab-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371ab-122">-ID</span><span class="sxs-lookup"><span data-stu-id="371ab-122">-Id</span></span>
<span data-ttu-id="371ab-123">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="371ab-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="371ab-124">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="371ab-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="371ab-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="371ab-125">-Name</span></span>
<span data-ttu-id="371ab-126">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="371ab-126">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="371ab-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="371ab-127">-Pre</span></span>
<span data-ttu-id="371ab-128">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="371ab-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371ab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="371ab-129">-ResourceGroupName</span></span>
<span data-ttu-id="371ab-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="371ab-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="371ab-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="371ab-131">-Confirm</span></span>
<span data-ttu-id="371ab-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="371ab-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371ab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="371ab-133">-WhatIf</span></span>
<span data-ttu-id="371ab-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="371ab-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="371ab-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="371ab-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371ab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371ab-136">CommonParameters</span></span>
<span data-ttu-id="371ab-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="371ab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371ab-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="371ab-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371ab-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="371ab-139">INPUTS</span></span>

### <span data-ttu-id="371ab-140">System. String</span><span class="sxs-lookup"><span data-stu-id="371ab-140">System.String</span></span>

## <span data-ttu-id="371ab-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="371ab-141">OUTPUTS</span></span>

### <span data-ttu-id="371ab-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="371ab-142">System.Boolean</span></span>

## <span data-ttu-id="371ab-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="371ab-143">NOTES</span></span>

## <span data-ttu-id="371ab-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="371ab-144">RELATED LINKS</span></span>
