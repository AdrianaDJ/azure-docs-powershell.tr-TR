---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: ee880422e01b68bb595c709c1642038f75003c49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933331"
---
# <span data-ttu-id="089d8-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="089d8-101">New-AzTag</span></span>

## <span data-ttu-id="089d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="089d8-102">SYNOPSIS</span></span>
<span data-ttu-id="089d8-103">Önceden tanımlanmış bir Azure etiketi oluşturur veya varolan bir etikete değerler ekler.</span><span class="sxs-lookup"><span data-stu-id="089d8-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

## <span data-ttu-id="089d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="089d8-104">SYNTAX</span></span>

```
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="089d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="089d8-105">DESCRIPTION</span></span>
<span data-ttu-id="089d8-106">**New-AzTag** cmdlet 'i önceden tanımlanmış bir önceden tanımlanmış değer Içeren bir Azure etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="089d8-106">The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="089d8-107">Önceden tanımlanmış varolan etiketlere başka değerler eklemek için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="089d8-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="089d8-108">Önceden tanımlanmış bir etiket oluşturmak için benzersiz bir etiket adı girin.</span><span class="sxs-lookup"><span data-stu-id="089d8-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="089d8-109">Önceden tanımlanmış varolan bir etikete değer eklemek için, varolan etiketin adını ve yeni değeri belirtin.</span><span class="sxs-lookup"><span data-stu-id="089d8-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="089d8-110">Bu cmdlet, değerleri ve uygulandığı kaynak sayısını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="089d8-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="089d8-111">**Yeni-AzTag** 'in bir parçası olduğu Azure Etiket modülü önceden tanımlanmış Azure etiketlerini yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="089d8-111">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="089d8-112">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="089d8-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="089d8-113">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="089d8-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="089d8-114">Kaynak veya kaynak grubuna önceden tanımlanmış bir etiket uygulamak için, New-AzTag cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="089d8-114">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="089d8-115">Belirtilen etiket adı veya adı olan kaynak gruplarını aramak için, Get-AzResourceGroup cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="089d8-115">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="089d8-116">Her etiketin bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="089d8-116">Every tag has a name.</span></span>
<span data-ttu-id="089d8-117">Değerler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="089d8-117">The values are optional.</span></span>
<span data-ttu-id="089d8-118">Önceden tanımlanmış bir Azure etiketinin birden çok değeri olabilir, ancak etiketi kaynak veya kaynak grubuna uyguladığınızda etiket adını ve yalnızca değerlerinden birini uygulayın.</span><span class="sxs-lookup"><span data-stu-id="089d8-118">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="089d8-119">Örneğin, finans, Insan kaynakları ve BT gibi her departman için bir değer içeren önceden tanımlanmış bir bölüm etiketi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="089d8-119">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="089d8-120">Bir kaynağa departman etiketini uyguladığınızda, finans gibi yalnızca önceden tanımlanmış bir değer uygulaındı.</span><span class="sxs-lookup"><span data-stu-id="089d8-120">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="089d8-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="089d8-121">EXAMPLES</span></span>

### <span data-ttu-id="089d8-122">Örnek 1: önceden tanımlanmış bir etiket oluşturma</span><span class="sxs-lookup"><span data-stu-id="089d8-122">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="089d8-123">Bu komut, FY2015 adında önceden tanımlanmış bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="089d8-123">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="089d8-124">Bu etikette değer yok.</span><span class="sxs-lookup"><span data-stu-id="089d8-124">This tag has no values.</span></span>
<span data-ttu-id="089d8-125">Bir kaynak veya kaynak grubuna değer içermeyen bir etiket uygulayabilir veya etikete değer eklemek için **New-AzTag** 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="089d8-125">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="089d8-126">Etiketi kaynağa veya kaynak grubuna uyguladığınızda de bir değer belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="089d8-126">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="089d8-127">Örnek 2: bir değer içeren önceden tanımlanmış bir etiket oluşturma</span><span class="sxs-lookup"><span data-stu-id="089d8-127">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="089d8-128">Bu komut, finans değeriyle bölüm adlı önceden tanımlanmış bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="089d8-128">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="089d8-129">Örnek 3: önceden tanımlanmış bir etikete değer ekleme</span><span class="sxs-lookup"><span data-stu-id="089d8-129">Example 3: Add a value to a predefined tag</span></span>
```
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

<span data-ttu-id="089d8-130">Bu komutlar, iki değerli bölüm adlı önceden tanımlanmış bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="089d8-130">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="089d8-131">Etiket adı varsa, **New-AzTag** , yeni bir tane oluşturmak yerine değeri varolan etikete ekler.</span><span class="sxs-lookup"><span data-stu-id="089d8-131">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="089d8-132">Örnek 4: önceden tanımlanmış etiket kullanma</span><span class="sxs-lookup"><span data-stu-id="089d8-132">Example 4: Use a predefined tag</span></span>
```
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

<span data-ttu-id="089d8-133">Bu örnekteki komutlar önceden tanımlanmış bir etiket oluşturur ve kullanılır.</span><span class="sxs-lookup"><span data-stu-id="089d8-133">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="089d8-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="089d8-134">PARAMETERS</span></span>

### <span data-ttu-id="089d8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089d8-135">-DefaultProfile</span></span>
<span data-ttu-id="089d8-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="089d8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="089d8-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="089d8-137">-Name</span></span>
<span data-ttu-id="089d8-138">Etiket adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="089d8-138">Specifies the tag name.</span></span>
<span data-ttu-id="089d8-139">Önceden tanımlanmış yeni bir etiket oluşturmak için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="089d8-139">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="089d8-140">Var olan etikete değer eklemek için var olan etiketin adını girin.</span><span class="sxs-lookup"><span data-stu-id="089d8-140">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="089d8-141">Önceden bir önceden tanımlanmış etiketin belirtilen adı varsa, **New-AzTag** , varsa, yeni etiket oluşturmak yerine bu adı içeren etikete (varsa) ekler.</span><span class="sxs-lookup"><span data-stu-id="089d8-141">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="089d8-142">-Değer</span><span class="sxs-lookup"><span data-stu-id="089d8-142">-Value</span></span>
<span data-ttu-id="089d8-143">Etiket değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="089d8-143">Specifies a tag value.</span></span>
<span data-ttu-id="089d8-144">Önceden tanımlanmış Etiketler birden çok değere sahip olabilir, ancak her komuta yalnızca bir değer girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="089d8-144">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="089d8-145">Bu parametre isteğe bağlıdır; çünkü Etiketler değer içermeyen adlara sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="089d8-145">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089d8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089d8-146">CommonParameters</span></span>
<span data-ttu-id="089d8-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="089d8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089d8-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="089d8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089d8-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="089d8-149">INPUTS</span></span>

### <span data-ttu-id="089d8-150">System. String</span><span class="sxs-lookup"><span data-stu-id="089d8-150">System.String</span></span>

## <span data-ttu-id="089d8-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="089d8-151">OUTPUTS</span></span>

### <span data-ttu-id="089d8-152">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="089d8-152">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="089d8-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="089d8-153">NOTES</span></span>

## <span data-ttu-id="089d8-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="089d8-154">RELATED LINKS</span></span>

[<span data-ttu-id="089d8-155">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="089d8-155">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="089d8-156">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="089d8-156">Remove-AzTag</span></span>](./Remove-AzTag.md)


