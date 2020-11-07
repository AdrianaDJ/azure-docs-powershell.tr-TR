---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: af8d117611eafbeaf79a107e0066ec60b58524e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932592"
---
# <span data-ttu-id="b4b06-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="b4b06-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="b4b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4b06-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b06-103">Yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="b4b06-103">Gets managed application definitions</span></span>

## <span data-ttu-id="b4b06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4b06-104">SYNTAX</span></span>

### <span data-ttu-id="b4b06-105">Getbynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4b06-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4b06-106">GetById</span><span class="sxs-lookup"><span data-stu-id="b4b06-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4b06-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4b06-107">DESCRIPTION</span></span>
<span data-ttu-id="b4b06-108">**Get-AzManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="b4b06-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="b4b06-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4b06-109">EXAMPLES</span></span>

### <span data-ttu-id="b4b06-110">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulama tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="b4b06-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="b4b06-111">Bu komut, yönetilen uygulama tanımlarını kaynak grubu "MyRG" altında alır</span><span class="sxs-lookup"><span data-stu-id="b4b06-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="b4b06-112">Örnek 2: yönetilen uygulama tanımı alma</span><span class="sxs-lookup"><span data-stu-id="b4b06-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="b4b06-113">Bu komut, kaynak grubu "MyRG" altındaki "myManagedAppDef" yönetilen uygulama tanımını alır</span><span class="sxs-lookup"><span data-stu-id="b4b06-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="b4b06-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4b06-114">PARAMETERS</span></span>

### <span data-ttu-id="b4b06-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="b4b06-115">-ApiVersion</span></span>
<span data-ttu-id="b4b06-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4b06-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b4b06-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b4b06-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b4b06-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b06-118">-DefaultProfile</span></span>
<span data-ttu-id="b4b06-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4b06-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b06-120">-ID</span><span class="sxs-lookup"><span data-stu-id="b4b06-120">-Id</span></span>
<span data-ttu-id="b4b06-121">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="b4b06-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="b4b06-122">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="b4b06-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b4b06-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4b06-123">-Name</span></span>
<span data-ttu-id="b4b06-124">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="b4b06-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="b4b06-125">-Pre-</span><span class="sxs-lookup"><span data-stu-id="b4b06-125">-Pre</span></span>
<span data-ttu-id="b4b06-126">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b06-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b4b06-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b06-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4b06-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b4b06-128">The resource group name.</span></span>

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

### <span data-ttu-id="b4b06-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b06-129">CommonParameters</span></span>
<span data-ttu-id="b4b06-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4b06-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b06-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b06-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b06-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4b06-132">INPUTS</span></span>

### <span data-ttu-id="b4b06-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b4b06-133">System.String</span></span>

## <span data-ttu-id="b4b06-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4b06-134">OUTPUTS</span></span>

### <span data-ttu-id="b4b06-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b4b06-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b4b06-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4b06-136">NOTES</span></span>

## <span data-ttu-id="b4b06-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4b06-137">RELATED LINKS</span></span>
