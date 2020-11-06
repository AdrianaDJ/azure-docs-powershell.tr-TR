---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
ms.openlocfilehash: ecea7ba6aa34df73de65a4d03e004531e81ff497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589350"
---
# <span data-ttu-id="5ad9c-101">Get-AzureRmDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="5ad9c-101">Get-AzureRmDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="5ad9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ad9c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad9c-103">Azure Güvenlik Merkezi tarafından keşfedilen güvenlik çözümlerini alır</span><span class="sxs-lookup"><span data-stu-id="5ad9c-103">Gets security solutions that were discovered by Azure Security Center</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ad9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ad9c-104">SYNTAX</span></span>

### <span data-ttu-id="5ad9c-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5ad9c-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ad9c-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5ad9c-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ad9c-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="5ad9c-107">ResourceId</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ad9c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ad9c-108">DESCRIPTION</span></span>
<span data-ttu-id="5ad9c-109">Güvenlik Çözümleri otomatik olarak Azure Güvenlik Merkezi tarafından keşfedilir; bu cmdlet 'i kullanarak keşfedilen güvenlik çözümlerini görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="5ad9c-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="5ad9c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ad9c-110">EXAMPLES</span></span>

### <span data-ttu-id="5ad9c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5ad9c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="5ad9c-112">Tüm keşfedilen güvenlik çözümlerini aboneliğe alın</span><span class="sxs-lookup"><span data-stu-id="5ad9c-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="5ad9c-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5ad9c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="5ad9c-114">Belirli bir güvenlik çözümünü edinme</span><span class="sxs-lookup"><span data-stu-id="5ad9c-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="5ad9c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ad9c-115">PARAMETERS</span></span>

### <span data-ttu-id="5ad9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad9c-116">-DefaultProfile</span></span>
<span data-ttu-id="5ad9c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ad9c-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="5ad9c-118">-Location</span></span>
<span data-ttu-id="5ad9c-119">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-119">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad9c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ad9c-120">-Name</span></span>
<span data-ttu-id="5ad9c-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5ad9c-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad9c-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5ad9c-124">-ResourceId</span></span>
<span data-ttu-id="5ad9c-125">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-125">Resource ID.</span></span>

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

### <span data-ttu-id="5ad9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad9c-126">CommonParameters</span></span>
<span data-ttu-id="5ad9c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ad9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad9c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ad9c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad9c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ad9c-129">INPUTS</span></span>

### <span data-ttu-id="5ad9c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5ad9c-130">System.String</span></span>

## <span data-ttu-id="5ad9c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ad9c-131">OUTPUTS</span></span>

### <span data-ttu-id="5ad9c-132">Microsoft. Azure. Commands. Security. model. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="5ad9c-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="5ad9c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ad9c-133">NOTES</span></span>

## <span data-ttu-id="5ad9c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ad9c-134">RELATED LINKS</span></span>
