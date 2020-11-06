---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: dd0bb1bb72aa1193cba75c44905be37a70b62d4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588383"
---
# <span data-ttu-id="561e4-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="561e4-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="561e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="561e4-102">SYNOPSIS</span></span>
<span data-ttu-id="561e4-103">Yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="561e4-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="561e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="561e4-104">SYNTAX</span></span>

### <span data-ttu-id="561e4-105">GetBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="561e4-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="561e4-106">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="561e4-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="561e4-107">GetById</span><span class="sxs-lookup"><span data-stu-id="561e4-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="561e4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="561e4-108">DESCRIPTION</span></span>
<span data-ttu-id="561e4-109">**Get-AzureRmManagedApplication** cmdlet 'i yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="561e4-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="561e4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="561e4-110">EXAMPLES</span></span>

### <span data-ttu-id="561e4-111">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="561e4-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="561e4-112">Bu komut, "MyRG" kaynak grubu altında yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="561e4-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="561e4-113">Örnek 2: tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="561e4-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="561e4-114">Bu komut, geçerli aboneliğin altındaki tüm yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="561e4-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="561e4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="561e4-115">PARAMETERS</span></span>

### <span data-ttu-id="561e4-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="561e4-116">-ApiVersion</span></span>
<span data-ttu-id="561e4-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="561e4-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="561e4-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="561e4-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="561e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="561e4-119">-DefaultProfile</span></span>
<span data-ttu-id="561e4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="561e4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="561e4-121">-ID</span><span class="sxs-lookup"><span data-stu-id="561e4-121">-Id</span></span>
<span data-ttu-id="561e4-122">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="561e4-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="561e4-123">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="561e4-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="561e4-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="561e4-124">-Name</span></span>
<span data-ttu-id="561e4-125">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="561e4-125">The managed application name.</span></span>

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

### <span data-ttu-id="561e4-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="561e4-126">-Pre</span></span>
<span data-ttu-id="561e4-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="561e4-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="561e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="561e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="561e4-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="561e4-129">The resource group name.</span></span>

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

### <span data-ttu-id="561e4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="561e4-130">CommonParameters</span></span>
<span data-ttu-id="561e4-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="561e4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="561e4-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="561e4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="561e4-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="561e4-133">INPUTS</span></span>

### <span data-ttu-id="561e4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="561e4-134">System.String</span></span>

## <span data-ttu-id="561e4-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="561e4-135">OUTPUTS</span></span>

### <span data-ttu-id="561e4-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="561e4-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="561e4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="561e4-137">NOTES</span></span>

## <span data-ttu-id="561e4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="561e4-138">RELATED LINKS</span></span>
