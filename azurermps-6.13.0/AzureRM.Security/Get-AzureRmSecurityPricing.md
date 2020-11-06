---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587162"
---
# <span data-ttu-id="f97a0-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="f97a0-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="f97a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f97a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f97a0-103">Bir kapsam için Azure Güvenlik Merkezi 'nin fiyatlandırma katmanı verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f97a0-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f97a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f97a0-104">SYNTAX</span></span>

### <span data-ttu-id="f97a0-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f97a0-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f97a0-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="f97a0-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f97a0-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="f97a0-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f97a0-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="f97a0-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f97a0-109">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f97a0-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f97a0-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="f97a0-110">DESCRIPTION</span></span>
<span data-ttu-id="f97a0-111">Azure Güvenlik Merkezi fiyatlandırma katmanı, bu cmdlet ile kapsamda belirlenir ve yapılandırılmış fiyatlandırma katmanlarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f97a0-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="f97a0-112">Abonelik fiyatlandırma katmanı, altındaki tüm kaynak gruplarını içerir.</span><span class="sxs-lookup"><span data-stu-id="f97a0-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="f97a0-113">Kaynak grubu fiyatlandırma katmanı, abonelik fiyatlandırma katmanını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="f97a0-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="f97a0-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f97a0-114">EXAMPLES</span></span>

### <span data-ttu-id="f97a0-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f97a0-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="f97a0-116">Aboneliğin tüm yapılandırılmış fiyatlandırma katmanlarını ve altındaki kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="f97a0-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="f97a0-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f97a0-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="f97a0-118">"MyService1" kaynak gorup için yapılandırılmış ücretlendirme katmanını alır.</span><span class="sxs-lookup"><span data-stu-id="f97a0-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="f97a0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f97a0-119">PARAMETERS</span></span>

### <span data-ttu-id="f97a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97a0-120">-DefaultProfile</span></span>
<span data-ttu-id="f97a0-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f97a0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f97a0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f97a0-122">-Name</span></span>
<span data-ttu-id="f97a0-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f97a0-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f97a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="f97a0-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f97a0-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97a0-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f97a0-126">-ResourceId</span></span>
<span data-ttu-id="f97a0-127">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f97a0-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f97a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97a0-128">CommonParameters</span></span>
<span data-ttu-id="f97a0-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f97a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97a0-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f97a0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97a0-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f97a0-131">INPUTS</span></span>

### <span data-ttu-id="f97a0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f97a0-132">System.String</span></span>

## <span data-ttu-id="f97a0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f97a0-133">OUTPUTS</span></span>

### <span data-ttu-id="f97a0-134">Microsoft. Azure. Commands. Security. model. pricing. Pssecurityprsosu</span><span class="sxs-lookup"><span data-stu-id="f97a0-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="f97a0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f97a0-135">NOTES</span></span>

## <span data-ttu-id="f97a0-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f97a0-136">RELATED LINKS</span></span>
