---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: aa93fee1aa1cf9242d87239625e1c25612498e09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759242"
---
# <span data-ttu-id="68330-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="68330-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="68330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68330-102">SYNOPSIS</span></span>
<span data-ttu-id="68330-103">Bir kapsam için Azure Güvenlik Merkezi 'nin fiyatlandırma katmanı verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="68330-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="68330-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68330-104">SYNTAX</span></span>

### <span data-ttu-id="68330-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68330-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68330-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="68330-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68330-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="68330-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68330-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="68330-108">DESCRIPTION</span></span>
<span data-ttu-id="68330-109">Azure Güvenlik Merkezi fiyatlandırma katmanı, bu cmdlet ile kapsamda belirlenir ve yapılandırılmış fiyatlandırma katmanlarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68330-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="68330-110">Abonelik fiyatlandırma katmanı, altındaki tüm kaynak gruplarını içerir.</span><span class="sxs-lookup"><span data-stu-id="68330-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="68330-111">Kaynak grubu fiyatlandırma katmanı, abonelik fiyatlandırma katmanını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="68330-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="68330-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68330-112">EXAMPLES</span></span>

### <span data-ttu-id="68330-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="68330-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="68330-114">Aboneliğin tüm yapılandırılmış fiyatlandırma katmanlarını ve altındaki kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="68330-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="68330-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="68330-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="68330-116">"MyService1" kaynak gorup için yapılandırılmış ücretlendirme katmanını alır.</span><span class="sxs-lookup"><span data-stu-id="68330-116">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="68330-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68330-117">PARAMETERS</span></span>

### <span data-ttu-id="68330-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68330-118">-DefaultProfile</span></span>
<span data-ttu-id="68330-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68330-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68330-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="68330-120">-Name</span></span>
<span data-ttu-id="68330-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="68330-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68330-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="68330-122">-ResourceId</span></span>
<span data-ttu-id="68330-123">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="68330-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68330-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68330-124">CommonParameters</span></span>
<span data-ttu-id="68330-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68330-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68330-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68330-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68330-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68330-127">INPUTS</span></span>

### <span data-ttu-id="68330-128">System. String</span><span class="sxs-lookup"><span data-stu-id="68330-128">System.String</span></span>

## <span data-ttu-id="68330-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68330-129">OUTPUTS</span></span>

### <span data-ttu-id="68330-130">Microsoft. Azure. Commands. Security. model. pricing. Pssecurityprsosu</span><span class="sxs-lookup"><span data-stu-id="68330-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="68330-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68330-131">NOTES</span></span>

## <span data-ttu-id="68330-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68330-132">RELATED LINKS</span></span>