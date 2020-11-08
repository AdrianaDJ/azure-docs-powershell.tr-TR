---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278002"
---
# <span data-ttu-id="c3ed7-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="c3ed7-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="c3ed7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ed7-103">Bir güvenlik değerlendirme türü oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="c3ed7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3ed7-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3ed7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ed7-106">Bir güvenlik değerlendirme meta verilerini oluşturur veya güncelleştirir, çeşitli değerlendirme özelliklerini oluşturmak ve yönetmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="c3ed7-107">Bu eylemden sonra, Bu abonelikteki herhangi bir kaynağa değerlendirme sonuçları rapor edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="c3ed7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3ed7-108">EXAMPLES</span></span>

### <span data-ttu-id="c3ed7-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c3ed7-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="c3ed7-110">Abonelikte yeni bir değerlendirme türü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="c3ed7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3ed7-111">PARAMETERS</span></span>

### <span data-ttu-id="c3ed7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ed7-112">-DefaultProfile</span></span>
<span data-ttu-id="c3ed7-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3ed7-114">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c3ed7-114">-Description</span></span>
<span data-ttu-id="c3ed7-115">Kullanıcıların bu değerlendirmenin anlamını ve nasıl hesaplandığını anlamasına yardımcı olacak ayrıntılı dize.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed7-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c3ed7-116">-DisplayName</span></span>
<span data-ttu-id="c3ed7-117">Bu nesne için okunabilir başlık.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-117">Human readable title for this object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3ed7-118">-Name</span></span>
<span data-ttu-id="c3ed7-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed7-120">-Çözüm açıklaması</span><span class="sxs-lookup"><span data-stu-id="c3ed7-120">-RemediationDescription</span></span>
<span data-ttu-id="c3ed7-121">Kullanıcıların güvenlik sorununu azaltmanın veya düzeltmenin farklı yollarını anlamasına yardımcı olacak ayrıntılı dize.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed7-122">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="c3ed7-122">-Severity</span></span>
<span data-ttu-id="c3ed7-123">Değerlendirme sağlıksız olduğunda güvenlik riskin önemini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ed7-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="c3ed7-124">-Confirm</span></span>
<span data-ttu-id="c3ed7-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3ed7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ed7-126">-WhatIf</span></span>
<span data-ttu-id="c3ed7-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3ed7-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3ed7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ed7-129">CommonParameters</span></span>
<span data-ttu-id="c3ed7-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ed7-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c3ed7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ed7-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3ed7-132">INPUTS</span></span>

### <span data-ttu-id="c3ed7-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c3ed7-133">None</span></span>

## <span data-ttu-id="c3ed7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3ed7-134">OUTPUTS</span></span>

### <span data-ttu-id="c3ed7-135">Microsoft. Azure. Commands. Security. modeller. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="c3ed7-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="c3ed7-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3ed7-136">NOTES</span></span>

## <span data-ttu-id="c3ed7-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3ed7-137">RELATED LINKS</span></span>
