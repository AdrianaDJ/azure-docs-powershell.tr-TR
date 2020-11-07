---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 909781b8cd441daab8bf5f567404a5e99e88cd0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764200"
---
# <span data-ttu-id="6cbc3-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="6cbc3-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="6cbc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbc3-103">Önceden tanımlanmış Azure etiketlerini veya değerlerini siler.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cbc3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6cbc3-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cbc3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6cbc3-105">DESCRIPTION</span></span>
<span data-ttu-id="6cbc3-106">**Remove-AzureRmTag** cmdlet 'i aboneliğinizden önceden tanımlanmış Azure etiketlerini ve değerlerini siler.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="6cbc3-107">Önceden tanımlanmış bir etiketten belirli değerleri silmek için, *değer* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="6cbc3-108">Varsayılan olarak, **Remove-AzureRmTag** belirtilen etiketi ve tüm değerlerini siler. Bir kaynağa veya kaynak grubuna uygulanmış olan bir etiketi veya değeri silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>

<span data-ttu-id="6cbc3-109">**Remove-AzureRmTag** 'i kullanmadan önce, kaynak veya kaynak grubundan etiket veya değerleri silmek için Set-AzureRMResourceGroup cmdlet 'in *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>

<span data-ttu-id="6cbc3-110">**-AzureRmTag** 'in parçası olan Azure Etiket modülü, önceden tanımlanmış Azure etiketlerinizi yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="6cbc3-111">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="6cbc3-112">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="6cbc3-113">Abonelik önceden tanımlanmış etiketler içeriyorsa, abonelikteki herhangi bir kaynak veya kaynak grubuna tanımsız Etiketler veya değerler uygulayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-113">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

## <span data-ttu-id="6cbc3-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6cbc3-114">EXAMPLES</span></span>

### <span data-ttu-id="6cbc3-115">Örnek 1: önceden tanımlanmış bir etiketi silme</span><span class="sxs-lookup"><span data-stu-id="6cbc3-115">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="6cbc3-116">Bu komut, Bölüm adlı önceden tanımlanmış etiketi ve tüm kaynaklarını siler.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-116">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="6cbc3-117">Etiket herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-117">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="6cbc3-118">Örnek 2: önceden tanımlanmış etiketten bir değer silme</span><span class="sxs-lookup"><span data-stu-id="6cbc3-118">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="6cbc3-119">Bu komut, önceden tanımlanmış Departman etiketinden HumanResources değerini siler.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-119">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="6cbc3-120">Etiketi silmez.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-120">It does not delete the tag.</span></span>
<span data-ttu-id="6cbc3-121">Değer herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-121">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="6cbc3-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6cbc3-122">PARAMETERS</span></span>

### <span data-ttu-id="6cbc3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6cbc3-123">-Name</span></span>
<span data-ttu-id="6cbc3-124">Silinecek etiketin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-124">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="6cbc3-125">Varsayılan olarak, **Remove-AzureRmTag** belirtilen etiketi ve tüm değerlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-125">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="6cbc3-126">Seçili değerleri silmek, ancak etiketi silistemiyorsanız *değer* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-126">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="6cbc3-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6cbc3-127">-PassThru</span></span>
<span data-ttu-id="6cbc3-128">Silinmiş etiketi veya sonuç etiketine sahip olan sonuç etiketini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-128">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="6cbc3-129">-Değer</span><span class="sxs-lookup"><span data-stu-id="6cbc3-129">-Value</span></span>
<span data-ttu-id="6cbc3-130">Önceden tanımlanmış etiketten belirtilen değerleri siler, ancak etiketi silmez.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-130">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="6cbc3-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6cbc3-131">-Confirm</span></span>
<span data-ttu-id="6cbc3-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cbc3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cbc3-133">-WhatIf</span></span>
<span data-ttu-id="6cbc3-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cbc3-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cbc3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbc3-136">-DefaultProfile</span></span>
<span data-ttu-id="6cbc3-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cbc3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbc3-138">CommonParameters</span></span>
<span data-ttu-id="6cbc3-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6cbc3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbc3-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cbc3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbc3-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6cbc3-141">INPUTS</span></span>

### <span data-ttu-id="6cbc3-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6cbc3-142">None</span></span>

## <span data-ttu-id="6cbc3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6cbc3-143">OUTPUTS</span></span>

### <span data-ttu-id="6cbc3-144">None veya Microsoft. Azure. Commands. Tags. model. PSTag</span><span class="sxs-lookup"><span data-stu-id="6cbc3-144">None or Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="6cbc3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6cbc3-145">NOTES</span></span>

## <span data-ttu-id="6cbc3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6cbc3-146">RELATED LINKS</span></span>

[<span data-ttu-id="6cbc3-147">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="6cbc3-147">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="6cbc3-148">Yeni-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="6cbc3-148">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


