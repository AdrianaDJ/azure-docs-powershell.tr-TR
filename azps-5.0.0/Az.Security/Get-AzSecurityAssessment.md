---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279464"
---
# <span data-ttu-id="a3d92-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a3d92-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="a3d92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3d92-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d92-103">Güvenlik değerlendirmelerini ve sonuçlarını bir abonelikle alır</span><span class="sxs-lookup"><span data-stu-id="a3d92-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="a3d92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3d92-104">SYNTAX</span></span>

### <span data-ttu-id="a3d92-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3d92-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3d92-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a3d92-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3d92-107">Resourceıdscope</span><span class="sxs-lookup"><span data-stu-id="a3d92-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3d92-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a3d92-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3d92-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3d92-109">DESCRIPTION</span></span>
<span data-ttu-id="a3d92-110">Güvenlik değerlendirmesini ve bunların sonuçlarını abonelikle alır.</span><span class="sxs-lookup"><span data-stu-id="a3d92-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="a3d92-111">Güvenlik değerlendirmeleri, Azure Güvenlik Merkezi tarafından Azure aboneliğinizde hangi en iyi uygulamaların azaltıldığından emin olduğunuzu size tanır.</span><span class="sxs-lookup"><span data-stu-id="a3d92-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="a3d92-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3d92-112">EXAMPLES</span></span>

### <span data-ttu-id="a3d92-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3d92-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="a3d92-114">Bir abonelikteki tüm güvenlik değerlendirmesini alır</span><span class="sxs-lookup"><span data-stu-id="a3d92-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="a3d92-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3d92-115">PARAMETERS</span></span>

### <span data-ttu-id="a3d92-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a3d92-116">-AssessedResourceId</span></span>
<span data-ttu-id="a3d92-117">Değerlendirmenin hesaplandığı kaynağın tam kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3d92-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3d92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d92-118">-DefaultProfile</span></span>
<span data-ttu-id="a3d92-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3d92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3d92-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3d92-120">-Name</span></span>
<span data-ttu-id="a3d92-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a3d92-121">Resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d92-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a3d92-122">-ResourceId</span></span>
<span data-ttu-id="a3d92-123">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3d92-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a3d92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d92-124">CommonParameters</span></span>
<span data-ttu-id="a3d92-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3d92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d92-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a3d92-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d92-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3d92-127">INPUTS</span></span>

### <span data-ttu-id="a3d92-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a3d92-128">System.String</span></span>

## <span data-ttu-id="a3d92-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3d92-129">OUTPUTS</span></span>

### <span data-ttu-id="a3d92-130">Microsoft. Azure. Commands. Security. modeller. değerlendirmeler. Pssecurityasa</span><span class="sxs-lookup"><span data-stu-id="a3d92-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="a3d92-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3d92-131">NOTES</span></span>

## <span data-ttu-id="a3d92-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3d92-132">RELATED LINKS</span></span>
