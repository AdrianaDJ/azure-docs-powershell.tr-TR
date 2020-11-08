---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 4adda2affcba1c29352f6fe9235a5f10a3c1382a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265782"
---
# <span data-ttu-id="88bd4-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="88bd4-101">Update-AzTag</span></span>

## <span data-ttu-id="88bd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88bd4-102">SYNOPSIS</span></span>

<span data-ttu-id="88bd4-103">Kaynak veya abonelikteki etiket kümesini seçmeli olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="88bd4-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="88bd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88bd4-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="88bd4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88bd4-105">DESCRIPTION</span></span>

<span data-ttu-id="88bd4-106">**RESOURCEID** 'ı olan **Update-aztag** cmdlet 'i, kaynak veya abonelikteki etiket kümesini seçerek güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="88bd4-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="88bd4-107">Bu işlem, belirtilen kaynakta veya abonelikte etiketleri değiştirmeye, birleştirmeye veya seçmeli olarak silmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="88bd4-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="88bd4-108">Belirtilen varlık, işlemin sonunda en fazla 50 etiketine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="88bd4-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="88bd4-109">' Değiştir ' seçeneği var olan tüm etiket kümesini yeni bir ayarla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="88bd4-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="88bd4-110">' Birleştir ' seçeneği, yeni adlarla etiket eklenmesine ve varolan adlarla etiketlerin değerlerini güncelleştirmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="88bd4-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="88bd4-111">' Sil ' seçeneği, belirli adlara veya ad/değer çiftlerine dayalı olarak etiketlerin silinmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="88bd4-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="88bd4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88bd4-112">EXAMPLES</span></span>

### <span data-ttu-id="88bd4-113">Örnek 1: "Birleştir" Işlemiyle bir abonelikteki etiket kümesini seçmeli olarak güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="88bd4-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="88bd4-114">Bu komut, abonelikteki etiket kümesini {subId} ile birleştirir.</span><span class="sxs-lookup"><span data-stu-id="88bd4-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="88bd4-115">Örnek 2: bir abonelikteki etiket kümesini "Replace" Işlemiyle seçmeli olarak güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="88bd4-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="88bd4-116">Bu komut, abonelikteki etiket kümesini {subId} ile birlikte ekleyin.</span><span class="sxs-lookup"><span data-stu-id="88bd4-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="88bd4-117">Örnek 3: "Sil" Işlemiyle bir abonelikteki etiket kümesini seçmeli olarak güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="88bd4-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="88bd4-118">Bu komut, abonelikteki etiket kümesini {subId} ile siler.</span><span class="sxs-lookup"><span data-stu-id="88bd4-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="88bd4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88bd4-119">PARAMETERS</span></span>

### <span data-ttu-id="88bd4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bd4-120">-DefaultProfile</span></span>
<span data-ttu-id="88bd4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88bd4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88bd4-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="88bd4-122">-ResourceId</span></span>
<span data-ttu-id="88bd4-123">Etiketli varlık için kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="88bd4-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="88bd4-124">Kaynak, kaynak grubu veya abonelik etiketleniyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="88bd4-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88bd4-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="88bd4-125">-Tag</span></span>
<span data-ttu-id="88bd4-126">Güncelleştirme için kullanılacak etiket kümesi.</span><span class="sxs-lookup"><span data-stu-id="88bd4-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88bd4-127">-İşlem</span><span class="sxs-lookup"><span data-stu-id="88bd4-127">-Operation</span></span>
<span data-ttu-id="88bd4-128">Güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="88bd4-128">The update operation.</span></span> <span data-ttu-id="88bd4-129">Seçenekler birleştirme, değiştirme ve silme.</span><span class="sxs-lookup"><span data-stu-id="88bd4-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88bd4-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="88bd4-130">-Confirm</span></span>
<span data-ttu-id="88bd4-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="88bd4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88bd4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88bd4-132">-WhatIf</span></span>
<span data-ttu-id="88bd4-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="88bd4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88bd4-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="88bd4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88bd4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bd4-135">CommonParameters</span></span>
<span data-ttu-id="88bd4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88bd4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bd4-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="88bd4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bd4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88bd4-138">INPUTS</span></span>

### <span data-ttu-id="88bd4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="88bd4-139">System.String</span></span>

### <span data-ttu-id="88bd4-140">Microsoft. Azure. Commands. Tags. model. TagPatchOpeation</span><span class="sxs-lookup"><span data-stu-id="88bd4-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation</span></span>

### <span data-ttu-id="88bd4-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="88bd4-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88bd4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88bd4-142">OUTPUTS</span></span>

### <span data-ttu-id="88bd4-143">Microsoft. Azure. Commands. Tags. model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="88bd4-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="88bd4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88bd4-144">NOTES</span></span>

## <span data-ttu-id="88bd4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88bd4-145">RELATED LINKS</span></span>

[<span data-ttu-id="88bd4-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="88bd4-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="88bd4-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="88bd4-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="88bd4-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="88bd4-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
