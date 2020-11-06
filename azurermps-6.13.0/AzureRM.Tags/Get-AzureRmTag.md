---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 945af88df11e210c3af3a11bd69123dd32befe4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594323"
---
# <span data-ttu-id="787c9-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="787c9-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="787c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="787c9-102">SYNOPSIS</span></span>
<span data-ttu-id="787c9-103">Önceden tanımlanmış Azure etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="787c9-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="787c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="787c9-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="787c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="787c9-105">DESCRIPTION</span></span>
<span data-ttu-id="787c9-106">**Get-AzureRmTag** cmdlet 'i aboneliğinizdeki önceden tanımlanmış Azure etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="787c9-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="787c9-107">Bu cmdlet etiketlerle ilgili temel bilgileri veya Etiketler ile değerleriyle ilgili ayrıntılı bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="787c9-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="787c9-108">Tüm çıktı nesneleri, etiketlerin ve değerlerin uygulandığı kaynak ve kaynak gruplarının sayısını temsil eden bir say özelliği içerir.</span><span class="sxs-lookup"><span data-stu-id="787c9-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="787c9-109">**Get-AzureRMTag** 'in bir parçası olduğu Azure Etiket modülü, önceden tanımlanmış Azure etiketlerini yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="787c9-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="787c9-110">Azure etiketi, Azure kaynaklarınızı ve Kaynak gruplarınızı bölüm veya maliyet merkezi olarak sınıflandırmak ya da kaynaklar ve gruplarla ilgili notları veya açıklamaları izlemek için kullanabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="787c9-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="787c9-111">Tek adımda etiketleri tanımlayabilir ve uygulayabilirsiniz, ancak önceden tanımlanmış Etiketler, aboneliğinizde etiketlerin standart, tutarlı, öngörülebilir adlarını ve değerlerini kurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="787c9-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="787c9-112">Önceden tanımlanmış bir etiket oluşturmak için New-AzureRmTag cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="787c9-112">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="787c9-113">Kaynak grubuna önceden tanımlanmış bir etiket uygulamak için New-AzureRmTag cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="787c9-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="787c9-114">Belirli bir etiket adı veya adı ve değerinin kaynak gruplarını aramak için, Get-AzureRMResourceGroup cmdlet 'inin *etiket* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="787c9-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="787c9-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="787c9-115">EXAMPLES</span></span>

### <span data-ttu-id="787c9-116">Örnek 1: tüm önceden tanımlanmış etiketleri alma</span><span class="sxs-lookup"><span data-stu-id="787c9-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="787c9-117">Bu komut, abonelikteki tüm önceden tanımlanmış etiketleri alır.</span><span class="sxs-lookup"><span data-stu-id="787c9-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="787c9-118">Count özelliği, etiketlerin, abonelikteki kaynaklara ve kaynak gruplarına kaç kez uygulandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="787c9-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="787c9-119">Örnek 2: ada göre etiket alma</span><span class="sxs-lookup"><span data-stu-id="787c9-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="787c9-120">Bu komut, Bölüm etiketi ve değerleri hakkında ayrıntılı bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="787c9-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="787c9-121">Count özelliği, etiketlerin ve bu değerlerin her birinin abonelikteki kaynaklara ve kaynak gruplarına uygulanma sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="787c9-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="787c9-122">Örnek 3: tüm etiketlerin değerlerini alma</span><span class="sxs-lookup"><span data-stu-id="787c9-122">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

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

<span data-ttu-id="787c9-123">Bu komut, abonelikteki tüm önceden tanımlanmış etiketlerle ilgili ayrıntılı bilgi almak için *ayrıntılı* parametreyi kullanır.</span><span class="sxs-lookup"><span data-stu-id="787c9-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="787c9-124">*Detailed* parametresini kullanmak, her etiket için *Name* parametresini kullanmanın eşdeğeridir.</span><span class="sxs-lookup"><span data-stu-id="787c9-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="787c9-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="787c9-125">PARAMETERS</span></span>

### <span data-ttu-id="787c9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787c9-126">-DefaultProfile</span></span>
<span data-ttu-id="787c9-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="787c9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="787c9-128">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="787c9-128">-Detailed</span></span>
<span data-ttu-id="787c9-129">Bu işlemin çıktıya etiket değerleri hakkında bilgi eklediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="787c9-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="787c9-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="787c9-130">-Name</span></span>
<span data-ttu-id="787c9-131">Alınacak etiketin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="787c9-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="787c9-132">**Get-AzureRmTag** varsayılan olarak, abonelikteki tüm önceden tanımlanmış etiketlerle ilgili temel bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="787c9-132">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="787c9-133">*Name* parametresini belirttiğinizde, *ayrıntılı* parametrenin etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="787c9-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="787c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787c9-134">CommonParameters</span></span>
<span data-ttu-id="787c9-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="787c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787c9-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="787c9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787c9-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="787c9-137">INPUTS</span></span>

### <span data-ttu-id="787c9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="787c9-138">System.String</span></span>

### <span data-ttu-id="787c9-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="787c9-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="787c9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="787c9-140">OUTPUTS</span></span>

### <span data-ttu-id="787c9-141">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="787c9-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="787c9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="787c9-142">NOTES</span></span>

## <span data-ttu-id="787c9-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="787c9-143">RELATED LINKS</span></span>

[<span data-ttu-id="787c9-144">Yeni-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="787c9-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="787c9-145">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="787c9-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


