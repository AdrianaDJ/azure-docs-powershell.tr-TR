---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 1c7f55bb3f84051326cd102c1c12a2d978a79f71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764584"
---
# <span data-ttu-id="0789d-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="0789d-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="0789d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0789d-102">SYNOPSIS</span></span>
<span data-ttu-id="0789d-103">Önceden tanımlanmış Azure etiketlerini veya değerlerini siler.</span><span class="sxs-lookup"><span data-stu-id="0789d-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0789d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0789d-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0789d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0789d-105">DESCRIPTION</span></span>
<span data-ttu-id="0789d-106">**Remove-AzureRmTag** cmdlet 'i aboneliğinizden önceden tanımlanmış Azure etiketlerini ve değerlerini siler.</span><span class="sxs-lookup"><span data-stu-id="0789d-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="0789d-107">Önceden tanımlanmış bir etiketten belirli değerleri silmek için, *değer* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0789d-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="0789d-108">Varsayılan olarak, **Remove-AzureRmTag** belirtilen etiketi ve tüm değerlerini siler. Bir kaynağa veya kaynak grubuna uygulanmış olan bir etiketi veya değeri silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="0789d-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="0789d-109">**Remove-AzureRmTag** 'i kullanmadan önce, kaynak veya kaynak grubundan etiket veya değerleri silmek için Set-AzureRMResourceGroup cmdlet 'in *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0789d-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="0789d-110">**-AzureRmTag** 'in parçası olan Azure Etiket modülü, önceden tanımlanmış Azure etiketlerinizi yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0789d-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="0789d-111">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="0789d-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="0789d-112">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="0789d-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="0789d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0789d-113">EXAMPLES</span></span>

### <span data-ttu-id="0789d-114">Örnek 1: önceden tanımlanmış bir etiketi silme</span><span class="sxs-lookup"><span data-stu-id="0789d-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="0789d-115">Bu komut, Bölüm adlı önceden tanımlanmış etiketi ve tüm kaynaklarını siler.</span><span class="sxs-lookup"><span data-stu-id="0789d-115">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="0789d-116">Etiket herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="0789d-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="0789d-117">Örnek 2: önceden tanımlanmış etiketten bir değer silme</span><span class="sxs-lookup"><span data-stu-id="0789d-117">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="0789d-118">Bu komut, önceden tanımlanmış Departman etiketinden HumanResources değerini siler.</span><span class="sxs-lookup"><span data-stu-id="0789d-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="0789d-119">Etiketi silmez.</span><span class="sxs-lookup"><span data-stu-id="0789d-119">It does not delete the tag.</span></span>
<span data-ttu-id="0789d-120">Değer herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="0789d-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="0789d-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0789d-121">PARAMETERS</span></span>

### <span data-ttu-id="0789d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0789d-122">-DefaultProfile</span></span>
<span data-ttu-id="0789d-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0789d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0789d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="0789d-124">-Name</span></span>
<span data-ttu-id="0789d-125">Silinecek etiketin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0789d-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="0789d-126">Varsayılan olarak, **Remove-AzureRmTag** belirtilen etiketi ve tüm değerlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0789d-126">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="0789d-127">Seçili değerleri silmek, ancak etiketi silistemiyorsanız *değer* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0789d-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="0789d-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0789d-128">-PassThru</span></span>
<span data-ttu-id="0789d-129">Silinmiş etiketi veya sonuç etiketine sahip olan sonuç etiketini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0789d-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="0789d-130">-Değer</span><span class="sxs-lookup"><span data-stu-id="0789d-130">-Value</span></span>
<span data-ttu-id="0789d-131">Önceden tanımlanmış etiketten belirtilen değerleri siler, ancak etiketi silmez.</span><span class="sxs-lookup"><span data-stu-id="0789d-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="0789d-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="0789d-132">-Confirm</span></span>
<span data-ttu-id="0789d-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0789d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0789d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0789d-134">-WhatIf</span></span>
<span data-ttu-id="0789d-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0789d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0789d-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0789d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0789d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0789d-137">CommonParameters</span></span>
<span data-ttu-id="0789d-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0789d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0789d-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0789d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0789d-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0789d-140">INPUTS</span></span>

### <span data-ttu-id="0789d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0789d-141">System.String</span></span>

### <span data-ttu-id="0789d-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="0789d-142">System.String[]</span></span>

### <span data-ttu-id="0789d-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0789d-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0789d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0789d-144">OUTPUTS</span></span>

### <span data-ttu-id="0789d-145">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="0789d-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="0789d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0789d-146">NOTES</span></span>

## <span data-ttu-id="0789d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0789d-147">RELATED LINKS</span></span>

[<span data-ttu-id="0789d-148">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="0789d-148">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="0789d-149">Yeni-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="0789d-149">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


