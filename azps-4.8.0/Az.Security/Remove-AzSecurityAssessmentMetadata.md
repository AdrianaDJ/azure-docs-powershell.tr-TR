---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273967"
---
# <span data-ttu-id="dbf2b-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="dbf2b-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="dbf2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbf2b-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf2b-103">Bir abonelikten güvenlik değerlendirme meta verilerini siler.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="dbf2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbf2b-104">SYNTAX</span></span>

### <span data-ttu-id="dbf2b-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dbf2b-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf2b-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="dbf2b-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf2b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dbf2b-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf2b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbf2b-108">DESCRIPTION</span></span>
<span data-ttu-id="dbf2b-109">Bir abonelikten güvenlik değerlendirme meta verilerini siler.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="dbf2b-110">Bu eylem değerlendirme türünü ve aboneliğin tüm ilgili değerlendirme sonuçlarını silecektir.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="dbf2b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbf2b-111">EXAMPLES</span></span>

### <span data-ttu-id="dbf2b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dbf2b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="dbf2b-113">Abonelikten bir değerlendirme türü siler</span><span class="sxs-lookup"><span data-stu-id="dbf2b-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="dbf2b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbf2b-114">PARAMETERS</span></span>

### <span data-ttu-id="dbf2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf2b-115">-DefaultProfile</span></span>
<span data-ttu-id="dbf2b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf2b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbf2b-117">-InputObject</span></span>
<span data-ttu-id="dbf2b-118">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf2b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="dbf2b-119">-Name</span></span>
<span data-ttu-id="dbf2b-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-120">Resource name.</span></span>

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

### <span data-ttu-id="dbf2b-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dbf2b-121">-PassThru</span></span>
<span data-ttu-id="dbf2b-122">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-122">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf2b-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dbf2b-123">-ResourceId</span></span>
<span data-ttu-id="dbf2b-124">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="dbf2b-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="dbf2b-125">-Confirm</span></span>
<span data-ttu-id="dbf2b-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf2b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf2b-127">-WhatIf</span></span>
<span data-ttu-id="dbf2b-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf2b-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf2b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf2b-130">CommonParameters</span></span>
<span data-ttu-id="dbf2b-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf2b-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dbf2b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf2b-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbf2b-133">INPUTS</span></span>

### <span data-ttu-id="dbf2b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dbf2b-134">System.String</span></span>

### <span data-ttu-id="dbf2b-135">Microsoft. Azure. Commands. Security. modeller. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="dbf2b-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="dbf2b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbf2b-136">OUTPUTS</span></span>

### <span data-ttu-id="dbf2b-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbf2b-137">System.Boolean</span></span>

## <span data-ttu-id="dbf2b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbf2b-138">NOTES</span></span>

## <span data-ttu-id="dbf2b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbf2b-139">RELATED LINKS</span></span>
