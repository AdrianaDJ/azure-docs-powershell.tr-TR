---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: a1b07c5fb76d912ec117d42497f0d0b14bfb298c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276552"
---
# <span data-ttu-id="4b2ee-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="4b2ee-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="4b2ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b2ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4b2ee-103">Bir kapsam için Azure Güvenlik Merkezi 'nin fiyatlandırma katmanı verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="4b2ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b2ee-104">SYNTAX</span></span>

### <span data-ttu-id="4b2ee-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b2ee-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b2ee-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4b2ee-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b2ee-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="4b2ee-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b2ee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b2ee-108">DESCRIPTION</span></span>
<span data-ttu-id="4b2ee-109">Azure Güvenlik Merkezi fiyatlandırma katmanı, bu cmdlet ile kapsamda belirlenir ve yapılandırılmış fiyatlandırma katmanlarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="4b2ee-110">Abonelik fiyatlandırma katmanı, altındaki tüm kaynak gruplarını içerir.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="4b2ee-111">Kaynak grubu fiyatlandırma katmanı, abonelik fiyatlandırma katmanını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="4b2ee-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b2ee-112">EXAMPLES</span></span>

### <span data-ttu-id="4b2ee-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4b2ee-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
Id--/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines
--                                                                                                                             ----       -----------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServers
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServerVirtualMachin…
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults
```

<span data-ttu-id="4b2ee-114">Aboneliğin tüm yapılandırılmış fiyatlandırma katmanlarını ve altındaki kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="4b2ee-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4b2ee-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="4b2ee-116">"MyService1" kaynak grubu için yapılandırılmış ücretlendirme katmanını alır.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="4b2ee-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b2ee-117">PARAMETERS</span></span>

### <span data-ttu-id="4b2ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b2ee-118">-DefaultProfile</span></span>
<span data-ttu-id="4b2ee-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b2ee-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b2ee-120">-Name</span></span>
<span data-ttu-id="4b2ee-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-121">Resource name.</span></span>

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

### <span data-ttu-id="4b2ee-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4b2ee-122">-ResourceId</span></span>
<span data-ttu-id="4b2ee-123">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-123">Resource ID.</span></span>

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

### <span data-ttu-id="4b2ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b2ee-124">CommonParameters</span></span>
<span data-ttu-id="4b2ee-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b2ee-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4b2ee-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b2ee-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b2ee-127">INPUTS</span></span>

### <span data-ttu-id="4b2ee-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4b2ee-128">System.String</span></span>

## <span data-ttu-id="4b2ee-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b2ee-129">OUTPUTS</span></span>

### <span data-ttu-id="4b2ee-130">Microsoft. Azure. Commands. Security. model. pricing. Pssecurityprsosu</span><span class="sxs-lookup"><span data-stu-id="4b2ee-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="4b2ee-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b2ee-131">NOTES</span></span>

## <span data-ttu-id="4b2ee-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b2ee-132">RELATED LINKS</span></span>
