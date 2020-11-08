---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276729"
---
# <span data-ttu-id="594d1-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="594d1-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="594d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="594d1-102">SYNOPSIS</span></span>
<span data-ttu-id="594d1-103">Aboneliğin güvenlik değerlendirme sonucunu siler.</span><span class="sxs-lookup"><span data-stu-id="594d1-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="594d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="594d1-104">SYNTAX</span></span>

### <span data-ttu-id="594d1-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="594d1-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594d1-106">Resourceıdlevelresource</span><span class="sxs-lookup"><span data-stu-id="594d1-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594d1-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="594d1-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594d1-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="594d1-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="594d1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="594d1-109">DESCRIPTION</span></span>
<span data-ttu-id="594d1-110">Bir aboneliğin güvenlik değerlendirme sonucunu sildiğinde, genellikle bir haya silindiğinde veya değerlendirme artık belirli bir kaynakla ilgili olmadığında kullanılır</span><span class="sxs-lookup"><span data-stu-id="594d1-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="594d1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="594d1-111">EXAMPLES</span></span>

### <span data-ttu-id="594d1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="594d1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="594d1-113">Aboneliğin değerlendirme sonucunu silme</span><span class="sxs-lookup"><span data-stu-id="594d1-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="594d1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="594d1-114">PARAMETERS</span></span>

### <span data-ttu-id="594d1-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="594d1-115">-AssessedResourceId</span></span>
<span data-ttu-id="594d1-116">Değerlendirmenin hesaplandığı kaynağın tam kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="594d1-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594d1-117">-DefaultProfile</span></span>
<span data-ttu-id="594d1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="594d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="594d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="594d1-119">-InputObject</span></span>
<span data-ttu-id="594d1-120">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="594d1-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="594d1-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="594d1-121">-Name</span></span>
<span data-ttu-id="594d1-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="594d1-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d1-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="594d1-123">-PassThru</span></span>
<span data-ttu-id="594d1-124">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="594d1-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="594d1-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="594d1-125">-ResourceId</span></span>
<span data-ttu-id="594d1-126">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="594d1-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="594d1-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="594d1-127">-Confirm</span></span>
<span data-ttu-id="594d1-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="594d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="594d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="594d1-129">-WhatIf</span></span>
<span data-ttu-id="594d1-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="594d1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="594d1-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="594d1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="594d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594d1-132">CommonParameters</span></span>
<span data-ttu-id="594d1-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="594d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594d1-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="594d1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594d1-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="594d1-135">INPUTS</span></span>

### <span data-ttu-id="594d1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="594d1-136">System.String</span></span>

### <span data-ttu-id="594d1-137">Microsoft. Azure. Commands. Security. modeller. değerlendirmeler. Pssecurityasa</span><span class="sxs-lookup"><span data-stu-id="594d1-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="594d1-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="594d1-138">OUTPUTS</span></span>

### <span data-ttu-id="594d1-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="594d1-139">System.Boolean</span></span>

## <span data-ttu-id="594d1-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="594d1-140">NOTES</span></span>

## <span data-ttu-id="594d1-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="594d1-141">RELATED LINKS</span></span>
