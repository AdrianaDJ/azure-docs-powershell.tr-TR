---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268173"
---
# <span data-ttu-id="45597-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="45597-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="45597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45597-102">SYNOPSIS</span></span>
<span data-ttu-id="45597-103">Yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="45597-103">Gets managed application definitions</span></span>

## <span data-ttu-id="45597-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45597-104">SYNTAX</span></span>

### <span data-ttu-id="45597-105">Getbynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="45597-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45597-106">GetById</span><span class="sxs-lookup"><span data-stu-id="45597-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45597-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="45597-107">DESCRIPTION</span></span>
<span data-ttu-id="45597-108">**Get-AzManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="45597-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="45597-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45597-109">EXAMPLES</span></span>

### <span data-ttu-id="45597-110">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulama tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="45597-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="45597-111">Bu komut, yönetilen uygulama tanımlarını kaynak grubu "MyRG" altında alır</span><span class="sxs-lookup"><span data-stu-id="45597-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="45597-112">Örnek 2: yönetilen uygulama tanımı alma</span><span class="sxs-lookup"><span data-stu-id="45597-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="45597-113">Bu komut, kaynak grubu "MyRG" altındaki "myManagedAppDef" yönetilen uygulama tanımını alır</span><span class="sxs-lookup"><span data-stu-id="45597-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="45597-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45597-114">PARAMETERS</span></span>

### <span data-ttu-id="45597-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="45597-115">-ApiVersion</span></span>
<span data-ttu-id="45597-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="45597-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="45597-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="45597-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="45597-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45597-118">-DefaultProfile</span></span>
<span data-ttu-id="45597-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45597-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45597-120">-ID</span><span class="sxs-lookup"><span data-stu-id="45597-120">-Id</span></span>
<span data-ttu-id="45597-121">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="45597-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="45597-122">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="45597-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45597-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="45597-123">-Name</span></span>
<span data-ttu-id="45597-124">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="45597-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="45597-125">-Pre-</span><span class="sxs-lookup"><span data-stu-id="45597-125">-Pre</span></span>
<span data-ttu-id="45597-126">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="45597-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="45597-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45597-127">-ResourceGroupName</span></span>
<span data-ttu-id="45597-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="45597-128">The resource group name.</span></span>

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

### <span data-ttu-id="45597-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45597-129">CommonParameters</span></span>
<span data-ttu-id="45597-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45597-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45597-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45597-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45597-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45597-132">INPUTS</span></span>

### <span data-ttu-id="45597-133">System. String</span><span class="sxs-lookup"><span data-stu-id="45597-133">System.String</span></span>

## <span data-ttu-id="45597-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45597-134">OUTPUTS</span></span>

### <span data-ttu-id="45597-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="45597-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="45597-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45597-136">NOTES</span></span>

## <span data-ttu-id="45597-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45597-137">RELATED LINKS</span></span>
