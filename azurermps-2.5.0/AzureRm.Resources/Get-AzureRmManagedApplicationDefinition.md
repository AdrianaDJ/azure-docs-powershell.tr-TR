---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: e6df93dee8599c6bae42cc9428b2a7691abf4740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939486"
---
# <span data-ttu-id="4c070-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="4c070-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="4c070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c070-102">SYNOPSIS</span></span>
<span data-ttu-id="4c070-103">Yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="4c070-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c070-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c070-104">SYNTAX</span></span>

### <span data-ttu-id="4c070-105">Getbynaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c070-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c070-106">GetById</span><span class="sxs-lookup"><span data-stu-id="4c070-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c070-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c070-107">DESCRIPTION</span></span>
<span data-ttu-id="4c070-108">**Get-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="4c070-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="4c070-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c070-109">EXAMPLES</span></span>

### <span data-ttu-id="4c070-110">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulama tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="4c070-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="4c070-111">Bu komut, yönetilen uygulama tanımlarını kaynak grubu "MyRG" altında alır</span><span class="sxs-lookup"><span data-stu-id="4c070-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="4c070-112">Örnek 2: yönetilen uygulama tanımı alma</span><span class="sxs-lookup"><span data-stu-id="4c070-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="4c070-113">Bu komut, kaynak grubu "MyRG" altındaki "myManagedAppDef" yönetilen uygulama tanımını alır</span><span class="sxs-lookup"><span data-stu-id="4c070-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="4c070-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c070-114">PARAMETERS</span></span>

### <span data-ttu-id="4c070-115">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="4c070-115">-ApiVersion</span></span>
<span data-ttu-id="4c070-116">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c070-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4c070-117">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c070-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4c070-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c070-118">-DefaultProfile</span></span>
<span data-ttu-id="4c070-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c070-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c070-120">-ID</span><span class="sxs-lookup"><span data-stu-id="4c070-120">-Id</span></span>
<span data-ttu-id="4c070-121">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="4c070-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="4c070-122">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="4c070-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c070-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c070-123">-Name</span></span>
<span data-ttu-id="4c070-124">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="4c070-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="4c070-125">-Pre-</span><span class="sxs-lookup"><span data-stu-id="4c070-125">-Pre</span></span>
<span data-ttu-id="4c070-126">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c070-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4c070-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c070-127">-ResourceGroupName</span></span>
<span data-ttu-id="4c070-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4c070-128">The resource group name.</span></span>

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

### <span data-ttu-id="4c070-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c070-129">CommonParameters</span></span>
<span data-ttu-id="4c070-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c070-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c070-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c070-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c070-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c070-132">INPUTS</span></span>

### <span data-ttu-id="4c070-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4c070-133">System.String</span></span>

## <span data-ttu-id="4c070-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c070-134">OUTPUTS</span></span>

### <span data-ttu-id="4c070-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4c070-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4c070-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c070-136">NOTES</span></span>

## <span data-ttu-id="4c070-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c070-137">RELATED LINKS</span></span>
