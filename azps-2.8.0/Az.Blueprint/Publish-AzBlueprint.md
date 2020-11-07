---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 5286b8953a9f28c5e63fe176f19d9d885e9c1d06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753112"
---
# <span data-ttu-id="2430c-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="2430c-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="2430c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2430c-102">SYNOPSIS</span></span>
<span data-ttu-id="2430c-103">Blueprint uygulamasının yeni bir sürümünü yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="2430c-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="2430c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2430c-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2430c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2430c-105">DESCRIPTION</span></span>
<span data-ttu-id="2430c-106">Şeması tanımının yeni bir sürümünü yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="2430c-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="2430c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2430c-107">EXAMPLES</span></span>

### <span data-ttu-id="2430c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2430c-108">Example 1</span></span>
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
<span data-ttu-id="2430c-109">Şeması tanımının yeni bir sürümünü yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="2430c-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="2430c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2430c-110">PARAMETERS</span></span>

### <span data-ttu-id="2430c-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="2430c-111">-Blueprint</span></span>
<span data-ttu-id="2430c-112">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2430c-112">Blueprint object.</span></span>

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

### <span data-ttu-id="2430c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2430c-113">-DefaultProfile</span></span>
<span data-ttu-id="2430c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2430c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2430c-115">-Version</span><span class="sxs-lookup"><span data-stu-id="2430c-115">-Version</span></span>
<span data-ttu-id="2430c-116">Şeması tanımının sürümü.</span><span class="sxs-lookup"><span data-stu-id="2430c-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="2430c-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="2430c-117">-ChangeNote</span></span>
<span data-ttu-id="2430c-118">Bu şeması sürümünün içeriğini açıklayan notlar.</span><span class="sxs-lookup"><span data-stu-id="2430c-118">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="2430c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2430c-119">CommonParameters</span></span>
<span data-ttu-id="2430c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2430c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2430c-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2430c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2430c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2430c-122">INPUTS</span></span>

### <span data-ttu-id="2430c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2430c-123">System.String</span></span>

### <span data-ttu-id="2430c-124">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="2430c-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="2430c-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2430c-125">OUTPUTS</span></span>

### <span data-ttu-id="2430c-126">Microsoft. Azure. Commands. Blueprint. modeller. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="2430c-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="2430c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2430c-127">NOTES</span></span>

## <span data-ttu-id="2430c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2430c-128">RELATED LINKS</span></span>
