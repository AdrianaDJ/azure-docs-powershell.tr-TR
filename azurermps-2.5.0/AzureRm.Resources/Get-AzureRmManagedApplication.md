---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 482bf9a2158fc299d78c993255e390dc480245a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939488"
---
# <span data-ttu-id="8641d-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="8641d-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="8641d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8641d-102">SYNOPSIS</span></span>
<span data-ttu-id="8641d-103">Yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="8641d-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8641d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8641d-104">SYNTAX</span></span>

### <span data-ttu-id="8641d-105">GetBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8641d-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8641d-106">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="8641d-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8641d-107">GetById</span><span class="sxs-lookup"><span data-stu-id="8641d-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8641d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8641d-108">DESCRIPTION</span></span>
<span data-ttu-id="8641d-109">**Get-AzureRmManagedApplication** cmdlet 'i yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="8641d-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="8641d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8641d-110">EXAMPLES</span></span>

### <span data-ttu-id="8641d-111">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="8641d-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="8641d-112">Bu komut, "MyRG" kaynak grubu altında yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="8641d-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="8641d-113">Örnek 2: tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="8641d-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="8641d-114">Bu komut, geçerli aboneliğin altındaki tüm yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="8641d-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="8641d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8641d-115">PARAMETERS</span></span>

### <span data-ttu-id="8641d-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8641d-116">-ApiVersion</span></span>
<span data-ttu-id="8641d-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="8641d-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8641d-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8641d-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8641d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8641d-119">-DefaultProfile</span></span>
<span data-ttu-id="8641d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8641d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8641d-121">-ID</span><span class="sxs-lookup"><span data-stu-id="8641d-121">-Id</span></span>
<span data-ttu-id="8641d-122">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="8641d-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="8641d-123">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="8641d-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8641d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="8641d-124">-Name</span></span>
<span data-ttu-id="8641d-125">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="8641d-125">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8641d-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="8641d-126">-Pre</span></span>
<span data-ttu-id="8641d-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8641d-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8641d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8641d-128">-ResourceGroupName</span></span>
<span data-ttu-id="8641d-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8641d-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8641d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8641d-130">CommonParameters</span></span>
<span data-ttu-id="8641d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8641d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8641d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8641d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8641d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8641d-133">INPUTS</span></span>

### <span data-ttu-id="8641d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8641d-134">System.String</span></span>

## <span data-ttu-id="8641d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8641d-135">OUTPUTS</span></span>

### <span data-ttu-id="8641d-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8641d-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8641d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8641d-137">NOTES</span></span>

## <span data-ttu-id="8641d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8641d-138">RELATED LINKS</span></span>
