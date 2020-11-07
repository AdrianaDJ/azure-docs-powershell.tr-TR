---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 3479a3d720554f0c062e2410d0c4b838f655909a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764005"
---
# <span data-ttu-id="bb73b-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="bb73b-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="bb73b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb73b-102">SYNOPSIS</span></span>
<span data-ttu-id="bb73b-103">Yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="bb73b-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb73b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb73b-104">SYNTAX</span></span>

### <span data-ttu-id="bb73b-105">Removebynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb73b-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb73b-106">Removebyıd</span><span class="sxs-lookup"><span data-stu-id="bb73b-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb73b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb73b-107">DESCRIPTION</span></span>
<span data-ttu-id="bb73b-108">**Remove-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="bb73b-108">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="bb73b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb73b-109">EXAMPLES</span></span>

### <span data-ttu-id="bb73b-110">Örnek 1: yönetilen uygulama tanımını kaynak KIMLIĞIYLE kaldırma</span><span class="sxs-lookup"><span data-stu-id="bb73b-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="bb73b-111">İlk komut, Get-AzureRmManagedApplicationDefinition cmdlet 'ini kullanarak myAppDef adlı bir yönetilen uygulama tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="bb73b-111">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="bb73b-112">Komut, $ApplicationDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bb73b-112">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="bb73b-113">İkinci komut, $ApplicationDefinition 'in **RESOURCEID** özelliğiyle tanımlanan yönetilen uygulama tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bb73b-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="bb73b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb73b-114">PARAMETERS</span></span>

### <span data-ttu-id="bb73b-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="bb73b-115">-ApiVersion</span></span>
<span data-ttu-id="bb73b-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb73b-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bb73b-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bb73b-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bb73b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb73b-118">-DefaultProfile</span></span>
<span data-ttu-id="bb73b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb73b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb73b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bb73b-120">-Force</span></span>
<span data-ttu-id="bb73b-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="bb73b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bb73b-122">-ID</span><span class="sxs-lookup"><span data-stu-id="bb73b-122">-Id</span></span>
<span data-ttu-id="bb73b-123">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="bb73b-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="bb73b-124">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="bb73b-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="bb73b-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb73b-125">-Name</span></span>
<span data-ttu-id="bb73b-126">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="bb73b-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="bb73b-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="bb73b-127">-Pre</span></span>
<span data-ttu-id="bb73b-128">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb73b-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bb73b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb73b-129">-ResourceGroupName</span></span>
<span data-ttu-id="bb73b-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bb73b-130">The resource group name.</span></span>

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

### <span data-ttu-id="bb73b-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb73b-131">-Confirm</span></span>
<span data-ttu-id="bb73b-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb73b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb73b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb73b-133">-WhatIf</span></span>
<span data-ttu-id="bb73b-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb73b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb73b-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb73b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb73b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb73b-136">CommonParameters</span></span>
<span data-ttu-id="bb73b-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb73b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb73b-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb73b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb73b-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb73b-139">INPUTS</span></span>

### <span data-ttu-id="bb73b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bb73b-140">System.String</span></span>

## <span data-ttu-id="bb73b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb73b-141">OUTPUTS</span></span>

### <span data-ttu-id="bb73b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb73b-142">System.Boolean</span></span>

## <span data-ttu-id="bb73b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb73b-143">NOTES</span></span>

## <span data-ttu-id="bb73b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb73b-144">RELATED LINKS</span></span>
