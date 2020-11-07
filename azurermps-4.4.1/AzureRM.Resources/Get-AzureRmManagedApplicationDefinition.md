---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ef724c4d2e9771243058471c3ce2aebc944d2bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762412"
---
# <span data-ttu-id="d6372-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="d6372-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="d6372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6372-102">SYNOPSIS</span></span>
<span data-ttu-id="d6372-103">Yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="d6372-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6372-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6372-104">SYNTAX</span></span>

### <span data-ttu-id="d6372-105">Yönetilen uygulama tanımı adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="d6372-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="d6372-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="d6372-106">(Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6372-107">Yönetilen uygulama tanımı kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="d6372-107">The managed application definition Id parameter set.</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6372-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6372-108">DESCRIPTION</span></span>
<span data-ttu-id="d6372-109">**Get-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımlarını alır</span><span class="sxs-lookup"><span data-stu-id="d6372-109">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="d6372-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6372-110">EXAMPLES</span></span>

### <span data-ttu-id="d6372-111">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulama tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="d6372-111">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="d6372-112">Bu komut, yönetilen uygulama tanımlarını kaynak grubu "MyRG" altında alır</span><span class="sxs-lookup"><span data-stu-id="d6372-112">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="d6372-113">Örnek 2: yönetilen uygulama tanımı alma</span><span class="sxs-lookup"><span data-stu-id="d6372-113">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="d6372-114">Bu komut, kaynak grubu "MyRG" altındaki "myManagedAppDef" yönetilen uygulama tanımını alır</span><span class="sxs-lookup"><span data-stu-id="d6372-114">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="d6372-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6372-115">PARAMETERS</span></span>

### <span data-ttu-id="d6372-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="d6372-116">-ApiVersion</span></span>
<span data-ttu-id="d6372-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6372-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d6372-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d6372-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d6372-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6372-119">-DefaultProfile</span></span>
<span data-ttu-id="d6372-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6372-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6372-121">-ID</span><span class="sxs-lookup"><span data-stu-id="d6372-121">-Id</span></span>
<span data-ttu-id="d6372-122">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="d6372-122">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="d6372-123">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="d6372-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6372-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="d6372-124">-Name</span></span>
<span data-ttu-id="d6372-125">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="d6372-125">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6372-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="d6372-126">-Pre</span></span>
<span data-ttu-id="d6372-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6372-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d6372-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6372-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6372-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d6372-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6372-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6372-130">CommonParameters</span></span>
<span data-ttu-id="d6372-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6372-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6372-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6372-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6372-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6372-133">INPUTS</span></span>

### <span data-ttu-id="d6372-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d6372-134">System.String</span></span>

## <span data-ttu-id="d6372-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6372-135">OUTPUTS</span></span>

### <span data-ttu-id="d6372-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d6372-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d6372-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6372-137">NOTES</span></span>

## <span data-ttu-id="d6372-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6372-138">RELATED LINKS</span></span>

