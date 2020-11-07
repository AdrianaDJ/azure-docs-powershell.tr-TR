---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
ms.openlocfilehash: 75e750aa13df16deb5c281a5914a6c21a1740e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764244"
---
# <span data-ttu-id="46d92-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="46d92-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="46d92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46d92-102">SYNOPSIS</span></span>
<span data-ttu-id="46d92-103">Yönetilen uygulamayı kaldırır</span><span class="sxs-lookup"><span data-stu-id="46d92-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46d92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46d92-104">SYNTAX</span></span>

### <span data-ttu-id="46d92-105">Yönetilen uygulama adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="46d92-105">The managed application name parameter set.</span></span> <span data-ttu-id="46d92-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="46d92-106">(Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46d92-107">Yönetilen uygulama kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="46d92-107">The managed application Id parameter set.</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46d92-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="46d92-108">DESCRIPTION</span></span>
<span data-ttu-id="46d92-109">**Remove-AzureRmManagedApplication** cmdlet 'i yönetilen uygulamayı kaldırır</span><span class="sxs-lookup"><span data-stu-id="46d92-109">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="46d92-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46d92-110">EXAMPLES</span></span>

### <span data-ttu-id="46d92-111">Örnek 1: yönetilen uygulamayı kaynak KIMLIĞIYLE kaldırma</span><span class="sxs-lookup"><span data-stu-id="46d92-111">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="46d92-112">İlk komut, Uygulamam adlı bir yönetilen uygulamayı Get-AzureRmManagedApplication cmdlet 'i kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="46d92-112">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="46d92-113">Komut, $Application değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="46d92-113">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="46d92-114">İkinci komut $Application 'in **RESOURCEID** özelliğiyle tanımlanan yönetilen uygulamayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="46d92-114">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="46d92-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46d92-115">PARAMETERS</span></span>

### <span data-ttu-id="46d92-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="46d92-116">-ApiVersion</span></span>
<span data-ttu-id="46d92-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="46d92-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="46d92-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="46d92-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="46d92-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d92-119">-DefaultProfile</span></span>
<span data-ttu-id="46d92-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46d92-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d92-121">-Force</span><span class="sxs-lookup"><span data-stu-id="46d92-121">-Force</span></span>
<span data-ttu-id="46d92-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="46d92-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="46d92-123">-ID</span><span class="sxs-lookup"><span data-stu-id="46d92-123">-Id</span></span>
<span data-ttu-id="46d92-124">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="46d92-124">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="46d92-125">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="46d92-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d92-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="46d92-126">-Name</span></span>
<span data-ttu-id="46d92-127">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="46d92-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d92-128">-Pre-</span><span class="sxs-lookup"><span data-stu-id="46d92-128">-Pre</span></span>
<span data-ttu-id="46d92-129">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46d92-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="46d92-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d92-130">-ResourceGroupName</span></span>
<span data-ttu-id="46d92-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="46d92-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d92-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="46d92-132">-Confirm</span></span>
<span data-ttu-id="46d92-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46d92-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d92-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d92-134">-WhatIf</span></span>
<span data-ttu-id="46d92-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46d92-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d92-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46d92-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d92-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d92-137">CommonParameters</span></span>
<span data-ttu-id="46d92-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46d92-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d92-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d92-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d92-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46d92-140">INPUTS</span></span>

### <span data-ttu-id="46d92-141">System. String</span><span class="sxs-lookup"><span data-stu-id="46d92-141">System.String</span></span>

## <span data-ttu-id="46d92-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46d92-142">OUTPUTS</span></span>

### <span data-ttu-id="46d92-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46d92-143">System.Boolean</span></span>

## <span data-ttu-id="46d92-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46d92-144">NOTES</span></span>

## <span data-ttu-id="46d92-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46d92-145">RELATED LINKS</span></span>

