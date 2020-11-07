---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: f9afc10613024d99cfa6b03b260324b3e5d22586
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932533"
---
# <span data-ttu-id="18de5-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="18de5-101">Remove-AzTag</span></span>

## <span data-ttu-id="18de5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18de5-102">SYNOPSIS</span></span>
<span data-ttu-id="18de5-103">Önceden tanımlanmış Azure etiketlerini veya değerlerini siler.</span><span class="sxs-lookup"><span data-stu-id="18de5-103">Deletes predefined Azure tags or values.</span></span>

## <span data-ttu-id="18de5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18de5-104">SYNTAX</span></span>

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18de5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18de5-105">DESCRIPTION</span></span>
<span data-ttu-id="18de5-106">**Remove-AzTag** cmdlet 'i aboneliğinizden önceden tanımlanmış Azure etiketlerini ve değerlerini siler.</span><span class="sxs-lookup"><span data-stu-id="18de5-106">The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="18de5-107">Önceden tanımlanmış bir etiketten belirli değerleri silmek için, *değer* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="18de5-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="18de5-108">Varsayılan olarak, **Remove-AzTag** belirtilen etiketi ve tüm değerlerini siler. Bir kaynağa veya kaynak grubuna uygulanmış olan bir etiketi veya değeri silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="18de5-108">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="18de5-109">**Remove-AzTag** 'i kullanmadan önce, kaynak veya kaynak grubundan etiket veya değerleri silmek için Set-AzResourceGroup cmdlet 'in *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="18de5-109">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="18de5-110">**Remove-AzTag** olan Azure Tags modülü, önceden tanımlanmış Azure etiketlerinizi yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="18de5-110">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="18de5-111">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="18de5-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="18de5-112">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="18de5-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="18de5-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18de5-113">EXAMPLES</span></span>

### <span data-ttu-id="18de5-114">Örnek 1: önceden tanımlanmış bir etiketi silme</span><span class="sxs-lookup"><span data-stu-id="18de5-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="18de5-115">Bu komut, Bölüm adlı önceden tanımlanmış etiketi ve tüm kaynaklarını siler.</span><span class="sxs-lookup"><span data-stu-id="18de5-115">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="18de5-116">Etiket herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="18de5-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="18de5-117">Örnek 2: önceden tanımlanmış etiketten bir değer silme</span><span class="sxs-lookup"><span data-stu-id="18de5-117">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="18de5-118">Bu komut, önceden tanımlanmış Departman etiketinden HumanResources değerini siler.</span><span class="sxs-lookup"><span data-stu-id="18de5-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="18de5-119">Etiketi silmez.</span><span class="sxs-lookup"><span data-stu-id="18de5-119">It does not delete the tag.</span></span>
<span data-ttu-id="18de5-120">Değer herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="18de5-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="18de5-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18de5-121">PARAMETERS</span></span>

### <span data-ttu-id="18de5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18de5-122">-DefaultProfile</span></span>
<span data-ttu-id="18de5-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18de5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18de5-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="18de5-124">-Name</span></span>
<span data-ttu-id="18de5-125">Silinecek etiketin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18de5-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="18de5-126">Varsayılan olarak, **Remove-AzTag** belirtilen etiketi ve tüm değerlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18de5-126">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="18de5-127">Seçili değerleri silmek, ancak etiketi silistemiyorsanız *değer* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="18de5-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18de5-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="18de5-128">-PassThru</span></span>
<span data-ttu-id="18de5-129">Silinmiş etiketi veya sonuç etiketine sahip olan sonuç etiketini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="18de5-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18de5-130">-Değer</span><span class="sxs-lookup"><span data-stu-id="18de5-130">-Value</span></span>
<span data-ttu-id="18de5-131">Önceden tanımlanmış etiketten belirtilen değerleri siler, ancak etiketi silmez.</span><span class="sxs-lookup"><span data-stu-id="18de5-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18de5-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="18de5-132">-Confirm</span></span>
<span data-ttu-id="18de5-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18de5-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18de5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18de5-134">-WhatIf</span></span>
<span data-ttu-id="18de5-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18de5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18de5-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18de5-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18de5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18de5-137">CommonParameters</span></span>
<span data-ttu-id="18de5-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18de5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18de5-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18de5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18de5-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18de5-140">INPUTS</span></span>

### <span data-ttu-id="18de5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="18de5-141">System.String</span></span>

### <span data-ttu-id="18de5-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="18de5-142">System.String[]</span></span>

### <span data-ttu-id="18de5-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18de5-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18de5-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18de5-144">OUTPUTS</span></span>

### <span data-ttu-id="18de5-145">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="18de5-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="18de5-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18de5-146">NOTES</span></span>

## <span data-ttu-id="18de5-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18de5-147">RELATED LINKS</span></span>

[<span data-ttu-id="18de5-148">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="18de5-148">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="18de5-149">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="18de5-149">New-AzTag</span></span>](./New-AzTag.md)


