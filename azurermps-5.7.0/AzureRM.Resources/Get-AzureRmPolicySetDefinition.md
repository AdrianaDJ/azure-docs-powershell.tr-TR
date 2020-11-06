---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592906"
---
# <span data-ttu-id="bacd7-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="bacd7-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="bacd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bacd7-102">SYNOPSIS</span></span>
<span data-ttu-id="bacd7-103">İlke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bacd7-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bacd7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bacd7-104">SYNTAX</span></span>

### <span data-ttu-id="bacd7-105">GetBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bacd7-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bacd7-106">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="bacd7-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bacd7-107">GetById</span><span class="sxs-lookup"><span data-stu-id="bacd7-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bacd7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bacd7-108">DESCRIPTION</span></span>
<span data-ttu-id="bacd7-109">**Get-AzureRmPolicySetDefinition** cmdlet 'i, tüm ilke kümesi tanımlarını veya ad veya kimlikle tanımlanan belirli bir ilke kümesi tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="bacd7-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="bacd7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bacd7-110">EXAMPLES</span></span>

### <span data-ttu-id="bacd7-111">Örnek 1: tüm ilke kümesi tanımını alma</span><span class="sxs-lookup"><span data-stu-id="bacd7-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="bacd7-112">Bu komut, tüm ilke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bacd7-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="bacd7-113">Örnek 2: ada göre ilke kümesi tanımını alma</span><span class="sxs-lookup"><span data-stu-id="bacd7-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="bacd7-114">Bu komut, VMPolicyDefinition adındaki ilke kümesi tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="bacd7-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="bacd7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bacd7-115">PARAMETERS</span></span>

### <span data-ttu-id="bacd7-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="bacd7-116">-ApiVersion</span></span>
<span data-ttu-id="bacd7-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="bacd7-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bacd7-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bacd7-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bacd7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bacd7-119">-DefaultProfile</span></span>
<span data-ttu-id="bacd7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bacd7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bacd7-121">-ID</span><span class="sxs-lookup"><span data-stu-id="bacd7-121">-Id</span></span>
<span data-ttu-id="bacd7-122">Abonelik dahil tam nitelikli ilke kümesi tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="bacd7-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="bacd7-123">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="bacd7-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bacd7-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="bacd7-124">-Name</span></span>
<span data-ttu-id="bacd7-125">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="bacd7-125">The policy set definition name.</span></span>

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

### <span data-ttu-id="bacd7-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="bacd7-126">-Pre</span></span>
<span data-ttu-id="bacd7-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bacd7-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bacd7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bacd7-128">CommonParameters</span></span>
<span data-ttu-id="bacd7-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bacd7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bacd7-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bacd7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bacd7-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bacd7-131">INPUTS</span></span>

### <span data-ttu-id="bacd7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bacd7-132">System.String</span></span>

## <span data-ttu-id="bacd7-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bacd7-133">OUTPUTS</span></span>

### <span data-ttu-id="bacd7-134">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bacd7-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bacd7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bacd7-135">NOTES</span></span>

## <span data-ttu-id="bacd7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bacd7-136">RELATED LINKS</span></span>
