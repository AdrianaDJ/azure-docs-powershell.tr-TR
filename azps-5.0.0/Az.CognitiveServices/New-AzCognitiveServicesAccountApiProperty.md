---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321781"
---
# <span data-ttu-id="08001-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="08001-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="08001-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08001-102">SYNOPSIS</span></span>
<span data-ttu-id="08001-103">Yeni bir örnek oluşturma hizmetleri hesap Apıproperties örneği</span><span class="sxs-lookup"><span data-stu-id="08001-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="08001-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08001-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08001-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="08001-105">DESCRIPTION</span></span>
<span data-ttu-id="08001-106">Öğretici hizmet hesabı Apıproperties 'in yeni bir örneğini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="08001-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="08001-107">Apıproperties, yeni bir hesap oluştururken veya mevcut bir hesabı güncelleştirirken kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="08001-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="08001-108">Apıproperties bazı hesap türleri için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="08001-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="08001-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08001-109">EXAMPLES</span></span>

### <span data-ttu-id="08001-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="08001-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="08001-111">Yukarıdaki örnek, "QnaRuntimeEndpoint" API özelliğiyle bir QnAMaker hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08001-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="08001-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08001-112">PARAMETERS</span></span>

### <span data-ttu-id="08001-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08001-113">-DefaultProfile</span></span>
<span data-ttu-id="08001-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08001-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08001-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="08001-115">-Confirm</span></span>
<span data-ttu-id="08001-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08001-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08001-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08001-117">-WhatIf</span></span>
<span data-ttu-id="08001-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08001-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08001-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08001-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08001-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08001-120">CommonParameters</span></span>
<span data-ttu-id="08001-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08001-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08001-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="08001-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08001-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08001-123">INPUTS</span></span>

### <span data-ttu-id="08001-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="08001-124">None</span></span>

## <span data-ttu-id="08001-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08001-125">OUTPUTS</span></span>

### <span data-ttu-id="08001-126">Microsoft. Azure. Management. öğretici Bveservices. modeller.</span><span class="sxs-lookup"><span data-stu-id="08001-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="08001-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08001-127">NOTES</span></span>

## <span data-ttu-id="08001-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08001-128">RELATED LINKS</span></span>
