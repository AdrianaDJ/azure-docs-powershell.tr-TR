---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 3897282708c310d59dffba52b3f5abfdf78d5f77
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940005"
---
# <span data-ttu-id="f6756-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="f6756-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="f6756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6756-102">SYNOPSIS</span></span>
<span data-ttu-id="f6756-103">Yönetilen uygulamayı kaldırır</span><span class="sxs-lookup"><span data-stu-id="f6756-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6756-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6756-104">SYNTAX</span></span>

### <span data-ttu-id="f6756-105">Removebynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f6756-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6756-106">Removebyıd</span><span class="sxs-lookup"><span data-stu-id="f6756-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6756-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6756-107">DESCRIPTION</span></span>
<span data-ttu-id="f6756-108">**Remove-AzureRmManagedApplication** cmdlet 'i yönetilen uygulamayı kaldırır</span><span class="sxs-lookup"><span data-stu-id="f6756-108">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="f6756-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6756-109">EXAMPLES</span></span>

### <span data-ttu-id="f6756-110">Örnek 1: yönetilen uygulamayı kaynak KIMLIĞIYLE kaldırma</span><span class="sxs-lookup"><span data-stu-id="f6756-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="f6756-111">İlk komut, Uygulamam adlı bir yönetilen uygulamayı Get-AzureRmManagedApplication cmdlet 'i kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="f6756-111">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="f6756-112">Komut, $Application değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f6756-112">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="f6756-113">İkinci komut $Application 'in **RESOURCEID** özelliğiyle tanımlanan yönetilen uygulamayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6756-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="f6756-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6756-114">PARAMETERS</span></span>

### <span data-ttu-id="f6756-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="f6756-115">-ApiVersion</span></span>
<span data-ttu-id="f6756-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6756-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f6756-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f6756-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f6756-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6756-118">-DefaultProfile</span></span>
<span data-ttu-id="f6756-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6756-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6756-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f6756-120">-Force</span></span>
<span data-ttu-id="f6756-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="f6756-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f6756-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f6756-122">-Id</span></span>
<span data-ttu-id="f6756-123">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="f6756-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="f6756-124">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="f6756-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="f6756-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6756-125">-Name</span></span>
<span data-ttu-id="f6756-126">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="f6756-126">The managed application name.</span></span>

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

### <span data-ttu-id="f6756-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="f6756-127">-Pre</span></span>
<span data-ttu-id="f6756-128">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6756-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f6756-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6756-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6756-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f6756-130">The resource group name.</span></span>

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

### <span data-ttu-id="f6756-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6756-131">-Confirm</span></span>
<span data-ttu-id="f6756-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6756-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6756-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6756-133">-WhatIf</span></span>
<span data-ttu-id="f6756-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6756-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6756-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6756-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6756-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6756-136">CommonParameters</span></span>
<span data-ttu-id="f6756-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6756-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6756-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6756-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6756-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6756-139">INPUTS</span></span>

### <span data-ttu-id="f6756-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f6756-140">System.String</span></span>

## <span data-ttu-id="f6756-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6756-141">OUTPUTS</span></span>

### <span data-ttu-id="f6756-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6756-142">System.Boolean</span></span>

## <span data-ttu-id="f6756-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6756-143">NOTES</span></span>

## <span data-ttu-id="f6756-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6756-144">RELATED LINKS</span></span>
