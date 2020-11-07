---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: b5b7356a2cda001bb615700b38657cc0d3249ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763596"
---
# <span data-ttu-id="ea801-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="ea801-101">New-AzureRmTag</span></span>

## <span data-ttu-id="ea801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea801-102">SYNOPSIS</span></span>
<span data-ttu-id="ea801-103">Önceden tanımlanmış bir Azure etiketi oluşturur veya varolan bir etikete değerler ekler.</span><span class="sxs-lookup"><span data-stu-id="ea801-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea801-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea801-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea801-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea801-105">DESCRIPTION</span></span>
<span data-ttu-id="ea801-106">**New-AzureRmTag** cmdlet 'i önceden tanımlanmış bir önceden tanımlanmış değer Içeren bir Azure etiketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea801-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="ea801-107">Önceden tanımlanmış varolan etiketlere başka değerler eklemek için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea801-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="ea801-108">Önceden tanımlanmış bir etiket oluşturmak için benzersiz bir etiket adı girin.</span><span class="sxs-lookup"><span data-stu-id="ea801-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="ea801-109">Önceden tanımlanmış varolan bir etikete değer eklemek için, varolan etiketin adını ve yeni değeri belirtin.</span><span class="sxs-lookup"><span data-stu-id="ea801-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>

<span data-ttu-id="ea801-110">Bu cmdlet, değerleri ve uygulandığı kaynak sayısını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea801-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>

<span data-ttu-id="ea801-111">**Yeni-AzureRmTag** 'in bir parçası olduğu Azure Etiket modülü, önceden tanımlanmış Azure etiketlerini yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ea801-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="ea801-112">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="ea801-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="ea801-113">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="ea801-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="ea801-114">Abonelik önceden tanımlanmış etiketler içeriyorsa, abonelikteki herhangi bir kaynak veya kaynak grubuna tanımsız Etiketler veya değerler uygulayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="ea801-114">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="ea801-115">Kaynak veya kaynak grubuna önceden tanımlanmış bir etiket uygulamak için, New-AzureRmTag cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea801-115">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="ea801-116">Belirtilen etiket adı veya adı olan kaynak gruplarını aramak için, Get-AzureRMResourceGroup cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea801-116">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

<span data-ttu-id="ea801-117">Her etiketin bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="ea801-117">Every tag has a name.</span></span>
<span data-ttu-id="ea801-118">Değerler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ea801-118">The values are optional.</span></span>
<span data-ttu-id="ea801-119">Önceden tanımlanmış bir Azure etiketinin birden çok değeri olabilir, ancak etiketi kaynak veya kaynak grubuna uyguladığınızda etiket adını ve yalnızca değerlerinden birini uygulayın.</span><span class="sxs-lookup"><span data-stu-id="ea801-119">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="ea801-120">Örneğin, finans, Insan kaynakları ve BT gibi her departman için bir değer içeren önceden tanımlanmış bir bölüm etiketi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea801-120">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="ea801-121">Bir kaynağa departman etiketini uyguladığınızda, finans gibi yalnızca önceden tanımlanmış bir değer uygulaındı.</span><span class="sxs-lookup"><span data-stu-id="ea801-121">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="ea801-122">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea801-122">EXAMPLES</span></span>

### <span data-ttu-id="ea801-123">Örnek 1: önceden tanımlanmış bir etiket oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea801-123">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="ea801-124">Bu komut, FY2015 adında önceden tanımlanmış bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea801-124">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="ea801-125">Bu etikette değer yok.</span><span class="sxs-lookup"><span data-stu-id="ea801-125">This tag has no values.</span></span>
<span data-ttu-id="ea801-126">Bir kaynak veya kaynak grubuna değer içermeyen bir etiket uygulayabilir veya etikete değer eklemek için **New-AzureRmTag** 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea801-126">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="ea801-127">Etiketi kaynağa veya kaynak grubuna uyguladığınızda de bir değer belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea801-127">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="ea801-128">Örnek 2: bir değer içeren önceden tanımlanmış bir etiket oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea801-128">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="ea801-129">Bu komut, finans değeriyle bölüm adlı önceden tanımlanmış bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea801-129">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="ea801-130">Örnek 3: önceden tanımlanmış bir etikete değer ekleme</span><span class="sxs-lookup"><span data-stu-id="ea801-130">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="ea801-131">Bu komutlar, iki değerli bölüm adlı önceden tanımlanmış bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea801-131">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="ea801-132">Etiket adı varsa, **New-AzureRmTag** , yeni bir tane oluşturmak yerine değeri varolan etikete ekler.</span><span class="sxs-lookup"><span data-stu-id="ea801-132">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="ea801-133">Örnek 4: önceden tanımlanmış etiket kullanma</span><span class="sxs-lookup"><span data-stu-id="ea801-133">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="ea801-134">Bu örnekteki komutlar önceden tanımlanmış bir etiket oluşturur ve kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ea801-134">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="ea801-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea801-135">PARAMETERS</span></span>

### <span data-ttu-id="ea801-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea801-136">-Name</span></span>
<span data-ttu-id="ea801-137">Etiket adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea801-137">Specifies the tag name.</span></span>
<span data-ttu-id="ea801-138">Önceden tanımlanmış yeni bir etiket oluşturmak için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="ea801-138">To create a new predefined tag, enter a unique name.</span></span>

<span data-ttu-id="ea801-139">Var olan etikete değer eklemek için var olan etiketin adını girin.</span><span class="sxs-lookup"><span data-stu-id="ea801-139">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="ea801-140">Önceden bir önceden tanımlanmış etiketin belirtilen adı varsa, **New-AzureRmTag** belirtilen değeri (varsa) yeni etiket oluşturmak yerine bu adı içeren etikete ekler.</span><span class="sxs-lookup"><span data-stu-id="ea801-140">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="ea801-141">-Değer</span><span class="sxs-lookup"><span data-stu-id="ea801-141">-Value</span></span>
<span data-ttu-id="ea801-142">Etiket değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea801-142">Specifies a tag value.</span></span>
<span data-ttu-id="ea801-143">Önceden tanımlanmış Etiketler birden çok değere sahip olabilir, ancak her komuta yalnızca bir değer girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea801-143">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="ea801-144">Bu parametre isteğe bağlıdır; çünkü Etiketler değer içermeyen adlara sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="ea801-144">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="ea801-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea801-145">-DefaultProfile</span></span>
<span data-ttu-id="ea801-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea801-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea801-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea801-147">CommonParameters</span></span>
<span data-ttu-id="ea801-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea801-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea801-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea801-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea801-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea801-150">INPUTS</span></span>

### <span data-ttu-id="ea801-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ea801-151">None</span></span>

## <span data-ttu-id="ea801-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea801-152">OUTPUTS</span></span>

### <span data-ttu-id="ea801-153">Microsoft. Azure. Commands. Tags. model. PSTag</span><span class="sxs-lookup"><span data-stu-id="ea801-153">Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="ea801-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea801-154">NOTES</span></span>

## <span data-ttu-id="ea801-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea801-155">RELATED LINKS</span></span>

[<span data-ttu-id="ea801-156">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="ea801-156">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="ea801-157">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="ea801-157">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


