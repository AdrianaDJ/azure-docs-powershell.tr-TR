---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267642"
---
# <span data-ttu-id="52b3e-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="52b3e-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="52b3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="52b3e-103">Azure Güvenlik Merkezi tarafından keşfedilen güvenlik çözümlerini alır</span><span class="sxs-lookup"><span data-stu-id="52b3e-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="52b3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52b3e-104">SYNTAX</span></span>

### <span data-ttu-id="52b3e-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52b3e-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52b3e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="52b3e-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52b3e-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="52b3e-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52b3e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="52b3e-108">DESCRIPTION</span></span>
<span data-ttu-id="52b3e-109">Güvenlik Çözümleri otomatik olarak Azure Güvenlik Merkezi tarafından keşfedilir; bu cmdlet 'i kullanarak keşfedilen güvenlik çözümlerini görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="52b3e-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="52b3e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52b3e-110">EXAMPLES</span></span>

### <span data-ttu-id="52b3e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="52b3e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="52b3e-112">Tüm keşfedilen güvenlik çözümlerini aboneliğe alın</span><span class="sxs-lookup"><span data-stu-id="52b3e-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="52b3e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="52b3e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="52b3e-114">Belirli bir güvenlik çözümünü edinme</span><span class="sxs-lookup"><span data-stu-id="52b3e-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="52b3e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52b3e-115">PARAMETERS</span></span>

### <span data-ttu-id="52b3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b3e-116">-DefaultProfile</span></span>
<span data-ttu-id="52b3e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52b3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b3e-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="52b3e-118">-Location</span></span>
<span data-ttu-id="52b3e-119">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="52b3e-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b3e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="52b3e-120">-Name</span></span>
<span data-ttu-id="52b3e-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="52b3e-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b3e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b3e-122">-ResourceGroupName</span></span>
<span data-ttu-id="52b3e-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="52b3e-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b3e-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="52b3e-124">-ResourceId</span></span>
<span data-ttu-id="52b3e-125">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="52b3e-125">Resource ID.</span></span>

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

### <span data-ttu-id="52b3e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b3e-126">CommonParameters</span></span>
<span data-ttu-id="52b3e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52b3e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b3e-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="52b3e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b3e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52b3e-129">INPUTS</span></span>

### <span data-ttu-id="52b3e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="52b3e-130">System.String</span></span>

## <span data-ttu-id="52b3e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52b3e-131">OUTPUTS</span></span>

### <span data-ttu-id="52b3e-132">Microsoft. Azure. Commands. Security. model. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="52b3e-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="52b3e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52b3e-133">NOTES</span></span>

## <span data-ttu-id="52b3e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52b3e-134">RELATED LINKS</span></span>
