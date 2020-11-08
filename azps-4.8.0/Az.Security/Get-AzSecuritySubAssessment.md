---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266874"
---
# <span data-ttu-id="79f7b-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="79f7b-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="79f7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="79f7b-103">Bir abonelikle alt değerlendirme sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="79f7b-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="79f7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79f7b-104">SYNTAX</span></span>

### <span data-ttu-id="79f7b-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79f7b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79f7b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="79f7b-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79f7b-107">Resourceıdlevelresource</span><span class="sxs-lookup"><span data-stu-id="79f7b-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79f7b-108">Resourceıdscope</span><span class="sxs-lookup"><span data-stu-id="79f7b-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79f7b-109">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="79f7b-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79f7b-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="79f7b-110">DESCRIPTION</span></span>
<span data-ttu-id="79f7b-111">Bir abonelikle alt değerlendirme sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="79f7b-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="79f7b-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79f7b-112">EXAMPLES</span></span>

### <span data-ttu-id="79f7b-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="79f7b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="79f7b-114">Bir abonelikteki tüm alt değerlendirme sonuçlarını alır.</span><span class="sxs-lookup"><span data-stu-id="79f7b-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="79f7b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79f7b-115">PARAMETERS</span></span>

### <span data-ttu-id="79f7b-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="79f7b-116">-AssessedResourceId</span></span>
<span data-ttu-id="79f7b-117">Değerlendirmenin hesaplandığı kaynağın tam kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="79f7b-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f7b-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="79f7b-118">-AssessmentName</span></span>
<span data-ttu-id="79f7b-119">Değerlendirme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="79f7b-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f7b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f7b-120">-DefaultProfile</span></span>
<span data-ttu-id="79f7b-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79f7b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79f7b-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="79f7b-122">-Name</span></span>
<span data-ttu-id="79f7b-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="79f7b-123">Resource name.</span></span>

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
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f7b-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="79f7b-124">-ResourceId</span></span>
<span data-ttu-id="79f7b-125">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="79f7b-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="79f7b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f7b-126">CommonParameters</span></span>
<span data-ttu-id="79f7b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79f7b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f7b-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="79f7b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f7b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79f7b-129">INPUTS</span></span>

### <span data-ttu-id="79f7b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="79f7b-130">System.String</span></span>

## <span data-ttu-id="79f7b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79f7b-131">OUTPUTS</span></span>

### <span data-ttu-id="79f7b-132">Microsoft. Azure. Commands. Security. modeller. SubAssessments. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="79f7b-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="79f7b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79f7b-133">NOTES</span></span>

## <span data-ttu-id="79f7b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79f7b-134">RELATED LINKS</span></span>
