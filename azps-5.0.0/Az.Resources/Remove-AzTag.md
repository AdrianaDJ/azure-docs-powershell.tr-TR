---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279822"
---
# <span data-ttu-id="d1f91-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="d1f91-101">Remove-AzTag</span></span>

## <span data-ttu-id="d1f91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f91-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f91-103">Önceden tanımlanmış Azure etiketlerini veya değerlerini siler | Kaynağın veya aboneliğin tüm etiket kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="d1f91-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="d1f91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1f91-104">SYNTAX</span></span>

### <span data-ttu-id="d1f91-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1f91-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f91-106">Removebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d1f91-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="d1f91-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1f91-107">DESCRIPTION</span></span>

<span data-ttu-id="d1f91-108">**Removepredefinedtagset** : **Remove-aztag** cmdlet 'i aboneliğinizden önceden tanımlanmış Azure etiketlerini ve değerlerini siler.</span><span class="sxs-lookup"><span data-stu-id="d1f91-108">**RemovePredefinedTagSet** : The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="d1f91-109">Önceden tanımlanmış bir etiketten belirli değerleri silmek için, *değer* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d1f91-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="d1f91-110">Varsayılan olarak, **Remove-AzTag** belirtilen etiketi ve tüm değerlerini siler. Bir kaynağa veya kaynak grubuna uygulanmış olan bir etiketi veya değeri silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1f91-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="d1f91-111">**Remove-AzTag** 'i kullanmadan önce, kaynak veya kaynak grubundan etiket veya değerleri silmek için Set-AzResourceGroup cmdlet 'in *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d1f91-111">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="d1f91-112">**Remove-AzTag** olan Azure Tags modülü, önceden tanımlanmış Azure etiketlerinizi yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="d1f91-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="d1f91-113">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="d1f91-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="d1f91-114">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="d1f91-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="d1f91-115">**Removebyresourceıdparameterset** : **RESOURCEID** Içeren **Remove-aztag** cmdlet 'i, kaynak veya abonelikteki tüm etiket kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="d1f91-115">**RemoveByResourceIdParameterSet** : The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="d1f91-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1f91-116">EXAMPLES</span></span>

### <span data-ttu-id="d1f91-117">Örnek 1: önceden tanımlanmış bir etiketi silme</span><span class="sxs-lookup"><span data-stu-id="d1f91-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="d1f91-118">Bu komut, Bölüm adlı önceden tanımlanmış etiketi ve tüm değerlerini siler.</span><span class="sxs-lookup"><span data-stu-id="d1f91-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="d1f91-119">Etiket herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="d1f91-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="d1f91-120">Örnek 2: önceden tanımlanmış etiketten bir değer silme</span><span class="sxs-lookup"><span data-stu-id="d1f91-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="d1f91-121">Bu komut, önceden tanımlanmış Departman etiketinden HumanResources değerini siler.</span><span class="sxs-lookup"><span data-stu-id="d1f91-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="d1f91-122">Etiketi silmez.</span><span class="sxs-lookup"><span data-stu-id="d1f91-122">It does not delete the tag.</span></span>
<span data-ttu-id="d1f91-123">Değer herhangi bir kaynağa veya kaynak grubuna uygulanmışsa, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="d1f91-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="d1f91-124">Örnek 3: abonelikteki tüm etiket kümesini silme</span><span class="sxs-lookup"><span data-stu-id="d1f91-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="d1f91-125">Bu komut, abonelikteki tüm etiket kümesini {subId} ile siler.</span><span class="sxs-lookup"><span data-stu-id="d1f91-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="d1f91-126">"-Passın" içine geçirilmişse silinen nesneyi döndürmez.</span><span class="sxs-lookup"><span data-stu-id="d1f91-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="d1f91-127">Örnek 4: kaynaktaki tüm etiket kümesini silme</span><span class="sxs-lookup"><span data-stu-id="d1f91-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="d1f91-128">Bu komut, kaynaktaki tüm etiket kümesini {RESOURCEID} ile siler.</span><span class="sxs-lookup"><span data-stu-id="d1f91-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="d1f91-129">"-Passin" içinde geçiş yaparken silinmiş oject 'i döndürür.</span><span class="sxs-lookup"><span data-stu-id="d1f91-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="d1f91-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1f91-130">PARAMETERS</span></span>

### <span data-ttu-id="d1f91-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f91-131">-DefaultProfile</span></span>
<span data-ttu-id="d1f91-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1f91-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1f91-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1f91-133">-Name</span></span>
<span data-ttu-id="d1f91-134">Kaldırılacak önceden tanımlanmış etiketin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1f91-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="d1f91-135">Varsayılan olarak, **Remove-AzTag** belirtilen etiketi ve tüm değerlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d1f91-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="d1f91-136">Seçili değerleri silmek, ancak etiketi silistemiyorsanız *değer* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d1f91-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f91-137">-Değer</span><span class="sxs-lookup"><span data-stu-id="d1f91-137">-Value</span></span>
<span data-ttu-id="d1f91-138">Önceden tanımlanmış etiketten belirtilen değerleri siler, ancak etiketi silmez.</span><span class="sxs-lookup"><span data-stu-id="d1f91-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f91-139">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d1f91-139">-ResourceId</span></span>
<span data-ttu-id="d1f91-140">Etiketli varlık için kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d1f91-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="d1f91-141">Kaynak, kaynak grubu veya abonelik etiketleniyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="d1f91-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f91-142">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d1f91-142">-PassThru</span></span>
<span data-ttu-id="d1f91-143">Silinmiş etiketi veya sonuç etiketine sahip olan sonuç etiketini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d1f91-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="d1f91-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1f91-144">-Confirm</span></span>
<span data-ttu-id="d1f91-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1f91-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1f91-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f91-146">-WhatIf</span></span>
<span data-ttu-id="d1f91-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1f91-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1f91-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1f91-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1f91-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f91-149">CommonParameters</span></span>
<span data-ttu-id="d1f91-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1f91-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f91-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d1f91-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f91-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1f91-152">INPUTS</span></span>

### <span data-ttu-id="d1f91-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d1f91-153">System.String</span></span>

### <span data-ttu-id="d1f91-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="d1f91-154">System.String[]</span></span>

### <span data-ttu-id="d1f91-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1f91-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1f91-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1f91-156">OUTPUTS</span></span>

### <span data-ttu-id="d1f91-157">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="d1f91-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="d1f91-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1f91-158">NOTES</span></span>

## <span data-ttu-id="d1f91-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1f91-159">RELATED LINKS</span></span>

[<span data-ttu-id="d1f91-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="d1f91-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="d1f91-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="d1f91-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="d1f91-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="d1f91-162">Update-AzTag</span></span>](./Update-AzTag.md)