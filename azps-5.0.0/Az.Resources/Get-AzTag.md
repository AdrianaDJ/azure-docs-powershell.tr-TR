---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322897"
---
# <span data-ttu-id="7d3f7-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="7d3f7-101">Get-AzTag</span></span>

## <span data-ttu-id="7d3f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3f7-103">Önceden tanımlanmış Azure etiketlerini alır | Kaynağın veya aboneliğin tüm etiket kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="7d3f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d3f7-104">SYNTAX</span></span>

### <span data-ttu-id="7d3f7-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d3f7-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d3f7-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7d3f7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d3f7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d3f7-107">DESCRIPTION</span></span>

<span data-ttu-id="7d3f7-108">**Getpredefinedtagset** : **Get-aztag** cmdlet 'i aboneliğinizdeki önceden tanımlanmış Azure etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-108">**GetPredefinedTagSet** : The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="7d3f7-109">Bu cmdlet etiketlerle ilgili temel bilgileri veya Etiketler ile değerleriyle ilgili ayrıntılı bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="7d3f7-110">Tüm çıktı nesneleri, etiketlerin ve değerlerin uygulandığı kaynak ve kaynak gruplarının sayısını temsil eden bir say özelliği içerir.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="7d3f7-111">**Get-AzTag** 'in bir parçası olduğu Azure Etiket modülü önceden tanımlanmış Azure etiketlerini yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="7d3f7-112">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="7d3f7-113">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="7d3f7-114">Önceden tanımlanmış bir etiket oluşturmak için New-AzTag cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="7d3f7-115">Kaynak grubuna önceden tanımlanmış bir etiket uygulamak için New-AzTag cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="7d3f7-116">Belirli bir etiket adı veya adı ve değerinin kaynak gruplarını aramak için, Get-AzResourceGroup cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="7d3f7-117">**Getbyresourceıdparameterset** : **RESOURCEID** Içeren **Get-aztag** cmdlet 'i, bir kaynak veya abonelikteki tüm etiket kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-117">**GetByResourceIdParameterSet** : The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="7d3f7-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d3f7-118">EXAMPLES</span></span>

### <span data-ttu-id="7d3f7-119">Örnek 1: tüm önceden tanımlanmış etiketleri alma</span><span class="sxs-lookup"><span data-stu-id="7d3f7-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="7d3f7-120">Bu komut, abonelikteki tüm önceden tanımlanmış etiketleri alır.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="7d3f7-121">Count özelliği, etiketlerin, abonelikteki kaynaklara ve kaynak gruplarına kaç kez uygulandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="7d3f7-122">Örnek 2: ada göre etiket alma</span><span class="sxs-lookup"><span data-stu-id="7d3f7-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="7d3f7-123">Bu komut, Bölüm etiketi ve değerleri hakkında ayrıntılı bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="7d3f7-124">Count özelliği, etiketlerin ve bu değerlerin her birinin abonelikteki kaynaklara ve kaynak gruplarına uygulanma sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="7d3f7-125">Örnek 3: tüm etiketlerin değerlerini alma</span><span class="sxs-lookup"><span data-stu-id="7d3f7-125">Example 3: Get values of all tags</span></span>
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="7d3f7-126">Bu komut, abonelikteki tüm önceden tanımlanmış etiketlerle ilgili ayrıntılı bilgi almak için *ayrıntılı* parametreyi kullanır.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="7d3f7-127">*Detailed* parametresini kullanmak, her etiket için *Name* parametresini kullanmanın eşdeğeridir.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="7d3f7-128">Örnek 4: bir abonelikteki tüm etiket kümesini alma</span><span class="sxs-lookup"><span data-stu-id="7d3f7-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="7d3f7-129">Bu komut, {subId} ile abonelikteki tüm etiket kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="7d3f7-130">Örnek 5: kaynaktaki tüm etiket kümesini alma</span><span class="sxs-lookup"><span data-stu-id="7d3f7-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="7d3f7-131">Bu komut, {RESOURCEID} ile kaynaktaki tüm etiket kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="7d3f7-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d3f7-132">PARAMETERS</span></span>

### <span data-ttu-id="7d3f7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3f7-133">-DefaultProfile</span></span>
<span data-ttu-id="7d3f7-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d3f7-135">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="7d3f7-135">-Detailed</span></span>
<span data-ttu-id="7d3f7-136">Bu işlemin çıktıya etiket değerleri hakkında bilgi eklediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3f7-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d3f7-137">-Name</span></span>
<span data-ttu-id="7d3f7-138">Önceden tanımlanmış etiketin adı.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-138">Name of the predefined tag.</span></span>
<span data-ttu-id="7d3f7-139">**Get-AzTag** , varsayılan olarak, abonelikteki tüm önceden tanımlanmış etiketlerle ilgili temel bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="7d3f7-140">*Name* parametresini belirttiğinizde, *ayrıntılı* parametrenin etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3f7-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7d3f7-141">-ResourceId</span></span>
<span data-ttu-id="7d3f7-142">Etiketli varlık için kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="7d3f7-143">Kaynak, kaynak grubu veya abonelik etiketleniyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3f7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3f7-144">CommonParameters</span></span>
<span data-ttu-id="7d3f7-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3f7-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7d3f7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3f7-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d3f7-147">INPUTS</span></span>

### <span data-ttu-id="7d3f7-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7d3f7-148">System.String</span></span>

### <span data-ttu-id="7d3f7-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7d3f7-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7d3f7-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d3f7-150">OUTPUTS</span></span>

### <span data-ttu-id="7d3f7-151">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="7d3f7-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="7d3f7-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d3f7-152">NOTES</span></span>

## <span data-ttu-id="7d3f7-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d3f7-153">RELATED LINKS</span></span>

[<span data-ttu-id="7d3f7-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="7d3f7-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="7d3f7-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="7d3f7-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="7d3f7-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="7d3f7-156">Update-AzTag</span></span>](./Update-AzTag.md)
