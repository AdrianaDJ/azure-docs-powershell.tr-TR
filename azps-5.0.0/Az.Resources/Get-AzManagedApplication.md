---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275898"
---
# <span data-ttu-id="be87a-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="be87a-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="be87a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be87a-102">SYNOPSIS</span></span>
<span data-ttu-id="be87a-103">Yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="be87a-103">Gets managed applications</span></span>

## <span data-ttu-id="be87a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be87a-104">SYNTAX</span></span>

### <span data-ttu-id="be87a-105">GetBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be87a-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be87a-106">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="be87a-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be87a-107">GetById</span><span class="sxs-lookup"><span data-stu-id="be87a-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be87a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="be87a-108">DESCRIPTION</span></span>
<span data-ttu-id="be87a-109">**Get-AzManagedApplication** cmdlet 'i yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="be87a-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="be87a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be87a-110">EXAMPLES</span></span>

### <span data-ttu-id="be87a-111">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="be87a-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="be87a-112">Bu komut, "MyRG" kaynak grubu altında yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="be87a-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="be87a-113">Örnek 2: tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="be87a-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="be87a-114">Bu komut, geçerli aboneliğin altındaki tüm yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="be87a-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="be87a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be87a-115">PARAMETERS</span></span>

### <span data-ttu-id="be87a-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="be87a-116">-ApiVersion</span></span>
<span data-ttu-id="be87a-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="be87a-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="be87a-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="be87a-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="be87a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be87a-119">-DefaultProfile</span></span>
<span data-ttu-id="be87a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be87a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be87a-121">-ID</span><span class="sxs-lookup"><span data-stu-id="be87a-121">-Id</span></span>
<span data-ttu-id="be87a-122">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="be87a-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="be87a-123">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="be87a-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be87a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="be87a-124">-Name</span></span>
<span data-ttu-id="be87a-125">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="be87a-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be87a-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="be87a-126">-Pre</span></span>
<span data-ttu-id="be87a-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be87a-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="be87a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be87a-128">-ResourceGroupName</span></span>
<span data-ttu-id="be87a-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="be87a-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be87a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be87a-130">CommonParameters</span></span>
<span data-ttu-id="be87a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be87a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be87a-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="be87a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be87a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be87a-133">INPUTS</span></span>

### <span data-ttu-id="be87a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="be87a-134">System.String</span></span>

## <span data-ttu-id="be87a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be87a-135">OUTPUTS</span></span>

### <span data-ttu-id="be87a-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="be87a-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="be87a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be87a-137">NOTES</span></span>

## <span data-ttu-id="be87a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be87a-138">RELATED LINKS</span></span>
