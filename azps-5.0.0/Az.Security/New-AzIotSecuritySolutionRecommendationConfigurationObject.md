---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276194"
---
# <span data-ttu-id="7f696-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="7f696-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="7f696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f696-102">SYNOPSIS</span></span>
<span data-ttu-id="7f696-103">IoT güvenlik çözümü için yeni öneri yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="7f696-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="7f696-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f696-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f696-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f696-105">DESCRIPTION</span></span>
<span data-ttu-id="7f696-106">AzIotSecuritySolutionRecommendationConfigurationObject, IoT güvenlik çözümü için yeni bir öneri yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f696-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="7f696-107">Bu şekilde, öneri durumu, etkinleştirilmiş veya devre dışı bırakılmış olsun yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="7f696-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="7f696-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f696-108">EXAMPLES</span></span>

### <span data-ttu-id="7f696-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f696-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="7f696-110">Öneri türü için "IoT_ACRAuthentication"</span><span class="sxs-lookup"><span data-stu-id="7f696-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="7f696-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f696-111">PARAMETERS</span></span>

### <span data-ttu-id="7f696-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f696-112">-DefaultProfile</span></span>
<span data-ttu-id="7f696-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f696-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f696-114">Özellikli</span><span class="sxs-lookup"><span data-stu-id="7f696-114">-Enabled</span></span>
<span data-ttu-id="7f696-115">Durumları.</span><span class="sxs-lookup"><span data-stu-id="7f696-115">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f696-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="7f696-116">-RecommendationType</span></span>
<span data-ttu-id="7f696-117">Öneri türü.</span><span class="sxs-lookup"><span data-stu-id="7f696-117">Recommendation type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f696-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f696-118">CommonParameters</span></span>
<span data-ttu-id="7f696-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f696-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f696-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7f696-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f696-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f696-121">INPUTS</span></span>

### <span data-ttu-id="7f696-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7f696-122">None</span></span>

## <span data-ttu-id="7f696-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f696-123">OUTPUTS</span></span>

### <span data-ttu-id="7f696-124">Microsoft. Azure. Commands. Security. modeller. ıotsecuritysolutions. PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f696-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="7f696-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f696-125">NOTES</span></span>

## <span data-ttu-id="7f696-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f696-126">RELATED LINKS</span></span>
