---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 953a810585550ec8895fc9306f78633beb4846a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587799"
---
# <span data-ttu-id="8f4c3-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="8f4c3-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="8f4c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4c3-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4c3-103">Yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="8f4c3-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f4c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f4c3-104">SYNTAX</span></span>

### <span data-ttu-id="8f4c3-105">Tüm yönetilen uygulamalar parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-105">The list all managed applications parameter set.</span></span> <span data-ttu-id="8f4c3-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="8f4c3-106">(Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f4c3-107">Yönetilen uygulama adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-107">The managed application name parameter set.</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f4c3-108">Yönetilen uygulama kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-108">The managed application Id parameter set.</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f4c3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f4c3-109">DESCRIPTION</span></span>
<span data-ttu-id="8f4c3-110">**Get-AzureRmManagedApplication** cmdlet 'i yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="8f4c3-110">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="8f4c3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f4c3-111">EXAMPLES</span></span>

### <span data-ttu-id="8f4c3-112">Örnek 1: kaynak grubu altındaki tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="8f4c3-112">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="8f4c3-113">Bu komut, "MyRG" kaynak grubu altında yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="8f4c3-113">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="8f4c3-114">Örnek 2: tüm yönetilen uygulamaları alma</span><span class="sxs-lookup"><span data-stu-id="8f4c3-114">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="8f4c3-115">Bu komut, geçerli aboneliğin altındaki tüm yönetilen uygulamaları alır</span><span class="sxs-lookup"><span data-stu-id="8f4c3-115">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="8f4c3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f4c3-116">PARAMETERS</span></span>

### <span data-ttu-id="8f4c3-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8f4c3-117">-ApiVersion</span></span>
<span data-ttu-id="8f4c3-118">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f4c3-119">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8f4c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4c3-120">-DefaultProfile</span></span>
<span data-ttu-id="8f4c3-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f4c3-122">-ID</span><span class="sxs-lookup"><span data-stu-id="8f4c3-122">-Id</span></span>
<span data-ttu-id="8f4c3-123">Abonelik dahil, tam nitelikli yönetilen uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="8f4c3-124">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="8f4c3-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4c3-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f4c3-125">-Name</span></span>
<span data-ttu-id="8f4c3-126">Yönetilen uygulama adı.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4c3-127">-Pre-</span><span class="sxs-lookup"><span data-stu-id="8f4c3-127">-Pre</span></span>
<span data-ttu-id="8f4c3-128">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8f4c3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f4c3-129">-ResourceGroupName</span></span>
<span data-ttu-id="8f4c3-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4c3-131">CommonParameters</span></span>
<span data-ttu-id="8f4c3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f4c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4c3-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f4c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4c3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f4c3-134">INPUTS</span></span>

### <span data-ttu-id="8f4c3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8f4c3-135">System.String</span></span>

## <span data-ttu-id="8f4c3-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f4c3-136">OUTPUTS</span></span>

### <span data-ttu-id="8f4c3-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8f4c3-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8f4c3-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f4c3-138">NOTES</span></span>

## <span data-ttu-id="8f4c3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f4c3-139">RELATED LINKS</span></span>

