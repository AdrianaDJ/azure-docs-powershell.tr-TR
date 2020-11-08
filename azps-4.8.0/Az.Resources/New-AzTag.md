---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266442"
---
# <span data-ttu-id="7cb8c-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="7cb8c-101">New-AzTag</span></span>

## <span data-ttu-id="7cb8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb8c-103">Önceden tanımlanmış bir Azure etiketi oluşturur veya varolan bir etikete değerler ekler | Kaynağın veya aboneliğin tüm etiket kümesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="7cb8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7cb8c-104">SYNTAX</span></span>

### <span data-ttu-id="7cb8c-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb8c-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cb8c-106">Createbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7cb8c-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="7cb8c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7cb8c-107">DESCRIPTION</span></span>

<span data-ttu-id="7cb8c-108">**Createpredefinedtagset** : **New-aztag** cmdlet 'i, önceden tanımlanmış bir önceden tanımlanmış değer içeren bir Azure etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-108">**CreatePredefinedTagSet** : The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="7cb8c-109">Önceden tanımlanmış varolan etiketlere başka değerler eklemek için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="7cb8c-110">Önceden tanımlanmış bir etiket oluşturmak için benzersiz bir etiket adı girin.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="7cb8c-111">Önceden tanımlanmış varolan bir etikete değer eklemek için, varolan etiketin adını ve yeni değeri belirtin.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="7cb8c-112">Bu cmdlet, değerleri ve uygulandığı kaynak sayısını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="7cb8c-113">**Yeni-AzTag** 'in bir parçası olduğu Azure Etiket modülü önceden tanımlanmış Azure etiketlerini yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="7cb8c-114">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="7cb8c-115">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="7cb8c-116">Kaynak veya kaynak grubuna önceden tanımlanmış bir etiket uygulamak için, New-AzTag cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="7cb8c-117">Belirtilen etiket adı veya adı olan kaynak gruplarını aramak için, Get-AzResourceGroup cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="7cb8c-118">Her etiketin bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-118">Every tag has a name.</span></span>
<span data-ttu-id="7cb8c-119">Değerler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-119">The values are optional.</span></span>
<span data-ttu-id="7cb8c-120">Önceden tanımlanmış bir Azure etiketinin birden çok değeri olabilir, ancak etiketi kaynak veya kaynak grubuna uyguladığınızda etiket adını ve yalnızca değerlerinden birini uygulayın.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="7cb8c-121">Örneğin, finans, Insan kaynakları ve BT gibi her departman için bir değer içeren önceden tanımlanmış bir bölüm etiketi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="7cb8c-122">Bir kaynağa departman etiketini uyguladığınızda, finans gibi yalnızca önceden tanımlanmış bir değer uygulaındı.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="7cb8c-123">**Createbyresourceıdparameterset** : **RESOURCEID** Içeren **Yeni-aztag** cmdlet 'i kaynak veya abonelikteki tüm etiket kümesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-123">**CreateByResourceIdParameterSet** : The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="7cb8c-124">Bu işlem, belirtilen kaynakta veya abonelikte tüm etiket kümesinin eklenmesine veya değiştirilmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="7cb8c-125">Belirtilen varlık en çok 50 etiketine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="7cb8c-126">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7cb8c-126">EXAMPLES</span></span>

### <span data-ttu-id="7cb8c-127">Örnek 1: önceden tanımlanmış bir etiket oluşturma</span><span class="sxs-lookup"><span data-stu-id="7cb8c-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="7cb8c-128">Bu komut, FY2015 adında önceden tanımlanmış bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="7cb8c-129">Bu etikette değer yok.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-129">This tag has no values.</span></span>
<span data-ttu-id="7cb8c-130">Bir kaynak veya kaynak grubuna değer içermeyen bir etiket uygulayabilir veya etikete değer eklemek için **New-AzTag** 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="7cb8c-131">Etiketi kaynağa veya kaynak grubuna uyguladığınızda de bir değer belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="7cb8c-132">Örnek 2: bir değer içeren önceden tanımlanmış bir etiket oluşturma</span><span class="sxs-lookup"><span data-stu-id="7cb8c-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="7cb8c-133">Bu komut, finans değeriyle bölüm adlı önceden tanımlanmış bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="7cb8c-134">Örnek 3: önceden tanımlanmış bir etikete değer ekleme</span><span class="sxs-lookup"><span data-stu-id="7cb8c-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="7cb8c-135">Bu komutlar, iki değerli bölüm adlı önceden tanımlanmış bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="7cb8c-136">Etiket adı varsa, **New-AzTag** , yeni bir tane oluşturmak yerine değeri varolan etikete ekler.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="7cb8c-137">Örnek 4: önceden tanımlanmış etiket kullanma</span><span class="sxs-lookup"><span data-stu-id="7cb8c-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="7cb8c-138">Bu örnekteki komutlar önceden tanımlanmış bir etiket oluşturur ve kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="7cb8c-139">Örnek 5: bir abonelikteki etiket kümesinin tamamını oluşturur veya güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7cb8c-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="7cb8c-140">Bu komut, {subId} ile abonelikteki tüm etiket kümesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="7cb8c-141">Örnek 6: kaynakta tüm etiket kümesini oluşturur veya güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7cb8c-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="7cb8c-142">Bu komut, {RESOURCEID} ile kaynakta tüm etiket kümesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="7cb8c-143">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7cb8c-143">PARAMETERS</span></span>

### <span data-ttu-id="7cb8c-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb8c-144">-DefaultProfile</span></span>
<span data-ttu-id="7cb8c-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cb8c-146">-Ad</span><span class="sxs-lookup"><span data-stu-id="7cb8c-146">-Name</span></span>
<span data-ttu-id="7cb8c-147">Önceden tanımlanmış etiket adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="7cb8c-148">Önceden tanımlanmış yeni bir etiket oluşturmak için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="7cb8c-149">Var olan etikete değer eklemek için var olan etiketin adını girin.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="7cb8c-150">Önceden bir önceden tanımlanmış etiketin belirtilen adı varsa, **New-AzTag** , varsa, yeni etiket oluşturmak yerine bu adı içeren etikete (varsa) ekler.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb8c-151">-Değer</span><span class="sxs-lookup"><span data-stu-id="7cb8c-151">-Value</span></span>
<span data-ttu-id="7cb8c-152">Önceden tanımlanmış bir etiket değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="7cb8c-153">Önceden tanımlanmış Etiketler birden çok değere sahip olabilir, ancak her komuta yalnızca bir değer girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="7cb8c-154">Bu parametre isteğe bağlıdır; çünkü Etiketler değer içermeyen adlara sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb8c-155">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7cb8c-155">-ResourceId</span></span>
<span data-ttu-id="7cb8c-156">Etiketlendiği varlığın kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="7cb8c-157">Kaynak, kaynak grubu veya abonelik etiketleniyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb8c-158">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7cb8c-158">-Tag</span></span>
<span data-ttu-id="7cb8c-159">Kaynağa eklenecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb8c-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="7cb8c-160">-Confirm</span></span>
<span data-ttu-id="7cb8c-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb8c-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb8c-162">-WhatIf</span></span>
<span data-ttu-id="7cb8c-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb8c-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb8c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb8c-165">CommonParameters</span></span>
<span data-ttu-id="7cb8c-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb8c-167">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7cb8c-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb8c-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7cb8c-168">INPUTS</span></span>

### <span data-ttu-id="7cb8c-169">System. String</span><span class="sxs-lookup"><span data-stu-id="7cb8c-169">System.String</span></span>

### <span data-ttu-id="7cb8c-170">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7cb8c-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7cb8c-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7cb8c-171">OUTPUTS</span></span>

### <span data-ttu-id="7cb8c-172">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="7cb8c-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="7cb8c-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7cb8c-173">NOTES</span></span>

## <span data-ttu-id="7cb8c-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7cb8c-174">RELATED LINKS</span></span>

[<span data-ttu-id="7cb8c-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="7cb8c-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="7cb8c-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="7cb8c-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="7cb8c-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="7cb8c-177">Update-AzTag</span></span>](./Update-AzTag.md)
