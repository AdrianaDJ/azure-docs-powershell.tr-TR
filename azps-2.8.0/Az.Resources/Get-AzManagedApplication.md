---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: 9c670973c9fcff3cd9038809cb955efc32edeee0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932593"
---
# <span data-ttu-id="458ee-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="458ee-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="458ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="458ee-102">SYNOPSIS</span></span>
<span data-ttu-id="458ee-103">Yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="458ee-103">Gets managed applications</span></span>

## <span data-ttu-id="458ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="458ee-104">SYNTAX</span></span>

### <span data-ttu-id="458ee-105">GetBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="458ee-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="458ee-106">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="458ee-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="458ee-107">GetById</span><span class="sxs-lookup"><span data-stu-id="458ee-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="458ee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="458ee-108">DESCRIPTION</span></span>
<span data-ttu-id="458ee-109">**Get-AzManagedApplication** cmdlet 'i yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="458ee-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="458ee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="458ee-110">EXAMPLES</span></span>

### <span data-ttu-id="458ee-111">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="458ee-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="458ee-112">Bu komut, "MyRG" kaynak grubu altında yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="458ee-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="458ee-113">Örnek 2: tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="458ee-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="458ee-114">Bu komut, geçerli aboneliğin altındaki tüm yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="458ee-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="458ee-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="458ee-115">PARAMETERS</span></span>

### <span data-ttu-id="458ee-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="458ee-116">-ApiVersion</span></span>
<span data-ttu-id="458ee-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="458ee-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="458ee-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="458ee-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="458ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458ee-119">-DefaultProfile</span></span>
<span data-ttu-id="458ee-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="458ee-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="458ee-121">-ID</span><span class="sxs-lookup"><span data-stu-id="458ee-121">-Id</span></span>
<span data-ttu-id="458ee-122">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="458ee-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="458ee-123">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="458ee-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="458ee-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="458ee-124">-Name</span></span>
<span data-ttu-id="458ee-125">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="458ee-125">The managed application name.</span></span>

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

### <span data-ttu-id="458ee-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="458ee-126">-Pre</span></span>
<span data-ttu-id="458ee-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="458ee-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="458ee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="458ee-128">-ResourceGroupName</span></span>
<span data-ttu-id="458ee-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="458ee-129">The resource group name.</span></span>

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

### <span data-ttu-id="458ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458ee-130">CommonParameters</span></span>
<span data-ttu-id="458ee-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="458ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458ee-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="458ee-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458ee-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="458ee-133">INPUTS</span></span>

### <span data-ttu-id="458ee-134">System. String</span><span class="sxs-lookup"><span data-stu-id="458ee-134">System.String</span></span>

## <span data-ttu-id="458ee-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="458ee-135">OUTPUTS</span></span>

### <span data-ttu-id="458ee-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="458ee-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="458ee-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="458ee-137">NOTES</span></span>

## <span data-ttu-id="458ee-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="458ee-138">RELATED LINKS</span></span>
