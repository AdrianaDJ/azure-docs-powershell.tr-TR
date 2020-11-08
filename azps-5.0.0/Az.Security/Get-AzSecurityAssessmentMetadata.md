---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279462"
---
# <span data-ttu-id="44dfb-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="44dfb-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="44dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="44dfb-103">Bir abonelikteki güvenlik değerlendirme türlerini ve metadta 'i alır.</span><span class="sxs-lookup"><span data-stu-id="44dfb-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="44dfb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44dfb-104">SYNTAX</span></span>

### <span data-ttu-id="44dfb-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44dfb-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44dfb-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="44dfb-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44dfb-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="44dfb-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44dfb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="44dfb-108">DESCRIPTION</span></span>
<span data-ttu-id="44dfb-109">Bir abonelikteki güvenlik değerlendirme türlerini ve metadta 'i alır.</span><span class="sxs-lookup"><span data-stu-id="44dfb-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="44dfb-110">Güvenlik değerlendirme meta verileri, kullanıcının tanımlayayapabileceği Built-In değerlendirmeleri ve özel değerlendirme türlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="44dfb-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="44dfb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44dfb-111">EXAMPLES</span></span>

### <span data-ttu-id="44dfb-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44dfb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="44dfb-113">Tüm yerleşik değerlendirmeleri ve geçerli abonelikte yapılandırılmış olan özel değerlendirmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="44dfb-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="44dfb-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44dfb-114">PARAMETERS</span></span>

### <span data-ttu-id="44dfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44dfb-115">-DefaultProfile</span></span>
<span data-ttu-id="44dfb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44dfb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44dfb-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="44dfb-117">-Name</span></span>
<span data-ttu-id="44dfb-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="44dfb-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44dfb-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="44dfb-119">-ResourceId</span></span>
<span data-ttu-id="44dfb-120">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="44dfb-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="44dfb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44dfb-121">CommonParameters</span></span>
<span data-ttu-id="44dfb-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44dfb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44dfb-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="44dfb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44dfb-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44dfb-124">INPUTS</span></span>

### <span data-ttu-id="44dfb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="44dfb-125">System.String</span></span>

## <span data-ttu-id="44dfb-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44dfb-126">OUTPUTS</span></span>

### <span data-ttu-id="44dfb-127">Microsoft. Azure. Commands. Security. modeller. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="44dfb-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="44dfb-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44dfb-128">NOTES</span></span>

## <span data-ttu-id="44dfb-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44dfb-129">RELATED LINKS</span></span>
