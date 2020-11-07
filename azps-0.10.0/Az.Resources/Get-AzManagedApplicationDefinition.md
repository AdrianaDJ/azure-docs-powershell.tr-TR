---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 4623634d72e78ab62deca43da698d218ddb9276e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936444"
---
# <span data-ttu-id="621d3-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="621d3-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="621d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="621d3-102">SYNOPSIS</span></span>
<span data-ttu-id="621d3-103">Yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="621d3-103">Gets managed application definitions</span></span>

## <span data-ttu-id="621d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="621d3-104">SYNTAX</span></span>

### <span data-ttu-id="621d3-105">Getbynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="621d3-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="621d3-106">GetById</span><span class="sxs-lookup"><span data-stu-id="621d3-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="621d3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="621d3-107">DESCRIPTION</span></span>
<span data-ttu-id="621d3-108">**Get-AzManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="621d3-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="621d3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="621d3-109">EXAMPLES</span></span>

### <span data-ttu-id="621d3-110">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulama tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="621d3-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="621d3-111">Bu komut, yönetilen uygulama tanımlarını kaynak grubu "MyRG" altında alır</span><span class="sxs-lookup"><span data-stu-id="621d3-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="621d3-112">Örnek 2: yönetilen uygulama tanımı alma</span><span class="sxs-lookup"><span data-stu-id="621d3-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="621d3-113">Bu komut, kaynak grubu "MyRG" altındaki "myManagedAppDef" yönetilen uygulama tanımını alır</span><span class="sxs-lookup"><span data-stu-id="621d3-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="621d3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="621d3-114">PARAMETERS</span></span>

### <span data-ttu-id="621d3-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="621d3-115">-ApiVersion</span></span>
<span data-ttu-id="621d3-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="621d3-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="621d3-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="621d3-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="621d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621d3-118">-DefaultProfile</span></span>
<span data-ttu-id="621d3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="621d3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621d3-120">-ID</span><span class="sxs-lookup"><span data-stu-id="621d3-120">-Id</span></span>
<span data-ttu-id="621d3-121">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="621d3-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="621d3-122">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="621d3-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="621d3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="621d3-123">-Name</span></span>
<span data-ttu-id="621d3-124">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="621d3-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="621d3-125">-Pre-</span><span class="sxs-lookup"><span data-stu-id="621d3-125">-Pre</span></span>
<span data-ttu-id="621d3-126">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="621d3-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="621d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="621d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="621d3-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="621d3-128">The resource group name.</span></span>

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

### <span data-ttu-id="621d3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621d3-129">CommonParameters</span></span>
<span data-ttu-id="621d3-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="621d3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621d3-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="621d3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621d3-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="621d3-132">INPUTS</span></span>

### <span data-ttu-id="621d3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="621d3-133">System.String</span></span>

## <span data-ttu-id="621d3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="621d3-134">OUTPUTS</span></span>

### <span data-ttu-id="621d3-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="621d3-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="621d3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="621d3-136">NOTES</span></span>

## <span data-ttu-id="621d3-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="621d3-137">RELATED LINKS</span></span>
