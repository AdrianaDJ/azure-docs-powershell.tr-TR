---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: ce672284a3d9887fe52c33081f04a86e1e072405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933351"
---
# <span data-ttu-id="81719-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="81719-101">Get-AzTag</span></span>

## <span data-ttu-id="81719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81719-102">SYNOPSIS</span></span>
<span data-ttu-id="81719-103">Önceden tanımlanmış Azure etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="81719-103">Gets predefined Azure tags.</span></span>

## <span data-ttu-id="81719-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81719-104">SYNTAX</span></span>

```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81719-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81719-105">DESCRIPTION</span></span>
<span data-ttu-id="81719-106">**Get-Azetiket** cmdlet 'i aboneliğinizde önceden tanımlanmış Azure etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="81719-106">The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="81719-107">Bu cmdlet etiketlerle ilgili temel bilgileri veya Etiketler ile değerleriyle ilgili ayrıntılı bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="81719-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="81719-108">Tüm çıktı nesneleri, etiketlerin ve değerlerin uygulandığı kaynak ve kaynak gruplarının sayısını temsil eden bir say özelliği içerir.</span><span class="sxs-lookup"><span data-stu-id="81719-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="81719-109">**Get-AzTag** 'in bir parçası olduğu Azure Etiket modülü önceden tanımlanmış Azure etiketlerini yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="81719-109">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="81719-110">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="81719-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="81719-111">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="81719-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="81719-112">Önceden tanımlanmış bir etiket oluşturmak için New-AzTag cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="81719-112">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="81719-113">Kaynak grubuna önceden tanımlanmış bir etiket uygulamak için New-AzTag cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="81719-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="81719-114">Belirli bir etiket adı veya adı ve değerinin kaynak gruplarını aramak için, Get-AzResourceGroup cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="81719-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="81719-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81719-115">EXAMPLES</span></span>

### <span data-ttu-id="81719-116">Örnek 1: tüm önceden tanımlanmış etiketleri alma</span><span class="sxs-lookup"><span data-stu-id="81719-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="81719-117">Bu komut, abonelikteki tüm önceden tanımlanmış etiketleri alır.</span><span class="sxs-lookup"><span data-stu-id="81719-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="81719-118">Count özelliği, etiketlerin, abonelikteki kaynaklara ve kaynak gruplarına kaç kez uygulandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81719-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="81719-119">Örnek 2: ada göre etiket alma</span><span class="sxs-lookup"><span data-stu-id="81719-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="81719-120">Bu komut, Bölüm etiketi ve değerleri hakkında ayrıntılı bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="81719-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="81719-121">Count özelliği, etiketlerin ve bu değerlerin her birinin abonelikteki kaynaklara ve kaynak gruplarına uygulanma sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81719-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="81719-122">Örnek 3: tüm etiketlerin değerlerini alma</span><span class="sxs-lookup"><span data-stu-id="81719-122">Example 3: Get values of all tags</span></span>
```
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

<span data-ttu-id="81719-123">Bu komut, abonelikteki tüm önceden tanımlanmış etiketlerle ilgili ayrıntılı bilgi almak için *ayrıntılı* parametreyi kullanır.</span><span class="sxs-lookup"><span data-stu-id="81719-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="81719-124">*Detailed* parametresini kullanmak, her etiket için *Name* parametresini kullanmanın eşdeğeridir.</span><span class="sxs-lookup"><span data-stu-id="81719-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="81719-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81719-125">PARAMETERS</span></span>

### <span data-ttu-id="81719-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81719-126">-DefaultProfile</span></span>
<span data-ttu-id="81719-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81719-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81719-128">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="81719-128">-Detailed</span></span>
<span data-ttu-id="81719-129">Bu işlemin çıktıya etiket değerleri hakkında bilgi eklediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="81719-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="81719-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="81719-130">-Name</span></span>
<span data-ttu-id="81719-131">Alınacak etiketin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81719-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="81719-132">**Get-AzTag** , varsayılan olarak, abonelikteki tüm önceden tanımlanmış etiketlerle ilgili temel bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="81719-132">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="81719-133">*Name* parametresini belirttiğinizde, *ayrıntılı* parametrenin etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="81719-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81719-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81719-134">CommonParameters</span></span>
<span data-ttu-id="81719-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81719-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81719-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81719-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81719-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81719-137">INPUTS</span></span>

### <span data-ttu-id="81719-138">System. String</span><span class="sxs-lookup"><span data-stu-id="81719-138">System.String</span></span>

### <span data-ttu-id="81719-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81719-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81719-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81719-140">OUTPUTS</span></span>

### <span data-ttu-id="81719-141">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="81719-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="81719-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81719-142">NOTES</span></span>

## <span data-ttu-id="81719-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81719-143">RELATED LINKS</span></span>

[<span data-ttu-id="81719-144">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="81719-144">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="81719-145">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="81719-145">Remove-AzTag</span></span>](./Remove-AzTag.md)


