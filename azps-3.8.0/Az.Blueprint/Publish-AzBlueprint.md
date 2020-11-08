---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: e61beaa43f881aa148401ef91cd4cb37c1f18d88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096469"
---
# <span data-ttu-id="7f594-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="7f594-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="7f594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f594-102">SYNOPSIS</span></span>
<span data-ttu-id="7f594-103">Blueprint uygulamasının yeni bir sürümünü yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="7f594-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="7f594-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f594-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f594-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f594-105">DESCRIPTION</span></span>
<span data-ttu-id="7f594-106">Şeması tanımının yeni bir sürümünü yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="7f594-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="7f594-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f594-107">EXAMPLES</span></span>

### <span data-ttu-id="7f594-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f594-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```
<span data-ttu-id="7f594-109">Şeması tanımının yeni bir sürümünü yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="7f594-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="7f594-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f594-110">PARAMETERS</span></span>

### <span data-ttu-id="7f594-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="7f594-111">-Blueprint</span></span>
<span data-ttu-id="7f594-112">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7f594-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f594-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f594-113">-DefaultProfile</span></span>
<span data-ttu-id="7f594-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f594-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f594-115">-Version</span><span class="sxs-lookup"><span data-stu-id="7f594-115">-Version</span></span>
<span data-ttu-id="7f594-116">Şeması tanımının sürümü.</span><span class="sxs-lookup"><span data-stu-id="7f594-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="7f594-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="7f594-117">-ChangeNote</span></span>
<span data-ttu-id="7f594-118">Bu şeması sürümünün içeriğini açıklayan notlar.</span><span class="sxs-lookup"><span data-stu-id="7f594-118">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f594-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f594-119">CommonParameters</span></span>
<span data-ttu-id="7f594-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f594-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7f594-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f594-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f594-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f594-122">INPUTS</span></span>

### <span data-ttu-id="7f594-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7f594-123">System.String</span></span>

### <span data-ttu-id="7f594-124">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="7f594-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="7f594-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f594-125">OUTPUTS</span></span>

### <span data-ttu-id="7f594-126">Microsoft. Azure. Commands. Blueprint. modeller. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="7f594-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="7f594-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f594-127">NOTES</span></span>

## <span data-ttu-id="7f594-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f594-128">RELATED LINKS</span></span>
