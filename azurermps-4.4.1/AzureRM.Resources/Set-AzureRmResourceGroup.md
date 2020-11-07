---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: a6fa8a27bacf5504564703d8669616f748aa95d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764233"
---
# <span data-ttu-id="1c8cb-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c8cb-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="1c8cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8cb-103">Kaynak grubunda değişiklik yapar.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c8cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c8cb-104">SYNTAX</span></span>

### <span data-ttu-id="1c8cb-105">Ad temelinde kaynak grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="1c8cb-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="1c8cb-106">(Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c8cb-107">Kimliği temel alan kaynak grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-107">Lists the resource group based in the Id.</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c8cb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c8cb-108">DESCRIPTION</span></span>
<span data-ttu-id="1c8cb-109">**Set-AzureRmResourceGroup** cmdlet 'i, kaynak grubunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-109">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="1c8cb-110">Bu cmdlet 'i kaynak grubuna uygulanmış Azure etiketlerini eklemek, değiştirmek veya silmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-110">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="1c8cb-111">Etiketleri değiştirmek için kaynak grubunu ve *etiket* parametresini tanımlayacak *ad* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-111">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>

<span data-ttu-id="1c8cb-112">Bu cmdlet 'i kaynak grubunun adını değiştirmek için kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-112">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="1c8cb-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c8cb-113">EXAMPLES</span></span>

### <span data-ttu-id="1c8cb-114">Örnek 1: kaynak grubuna etiket uygulama</span><span class="sxs-lookup"><span data-stu-id="1c8cb-114">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="1c8cb-115">Bu komut, mevcut etiketleri olmayan bir kaynak grubuna bir değer içeren bir departman etiketi uygular.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-115">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="1c8cb-116">Örnek 2: kaynak grubuna etiket ekleme</span><span class="sxs-lookup"><span data-stu-id="1c8cb-116">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="1c8cb-117">Bu örnek, mevcut etiketleri olan kaynak grubuna onaylanmış bir değer ve bir FY2016 etiketi içeren bir durum etiketi ekler.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-117">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="1c8cb-118">Belirttiğiniz Etiketler var olan etiketlerin yerine, varolan etiketleri yeni etiket koleksiyonuna eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-118">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>

<span data-ttu-id="1c8cb-119">İlk komut ContosoRG kaynak grubunu alır ve etiket yöntemini kullanarak etiketleri özelliğinin değerini alır.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-119">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="1c8cb-120">Komut, etiketleri $Tags değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-120">The command stores the tags in the $Tags variable.</span></span>

<span data-ttu-id="1c8cb-121">İkinci komut $Tags değişkeninde etiketleri alır.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-121">The second command gets the tags in the $Tags variable.</span></span>

<span data-ttu-id="1c8cb-122">Üçüncü komut, FY2016 ve etiketlerini $Tags değişkeninde etiket dizisine eklemek için + = atama işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-122">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>

<span data-ttu-id="1c8cb-123">Dördüncü komut, ContosoRG kaynak grubuna $Tags değişkeninde etiketleri uygulamak için **set-AzureRmResourceGroup** *etiket* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-123">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>

<span data-ttu-id="1c8cb-124">Beşinci komut, ContosoRG kaynak grubuna uygulanan tüm etiketleri alır.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-124">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="1c8cb-125">Çıktıda, kaynak grubunda bölüm etiketi ve iki yeni etiket, durum ve FY2015 bulunur.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-125">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="1c8cb-126">Örnek 3: kaynak grubun tüm etiketlerini silme</span><span class="sxs-lookup"><span data-stu-id="1c8cb-126">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="1c8cb-127">Bu komut, ContosoRG kaynak grubundaki tüm etiketleri silmek için boş karma tablo değeri olan *Tag* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-127">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="1c8cb-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c8cb-128">PARAMETERS</span></span>

### <span data-ttu-id="1c8cb-129">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="1c8cb-129">-ApiVersion</span></span>
<span data-ttu-id="1c8cb-130">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-130">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1c8cb-131">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-131">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8cb-132">-ID</span><span class="sxs-lookup"><span data-stu-id="1c8cb-132">-Id</span></span>
<span data-ttu-id="1c8cb-133">Değiştirilecek kaynak grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-133">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8cb-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="1c8cb-134">-Name</span></span>
<span data-ttu-id="1c8cb-135">Değiştirilecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-135">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c8cb-136">-Pre-</span><span class="sxs-lookup"><span data-stu-id="1c8cb-136">-Pre</span></span>
<span data-ttu-id="1c8cb-137">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c8cb-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1c8cb-138">-Tag</span></span>
<span data-ttu-id="1c8cb-139">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1c8cb-140">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="1c8cb-140">For example:</span></span>

<span data-ttu-id="1c8cb-141">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1c8cb-141">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="1c8cb-142">Etiket, oluşturabileceğiniz ve kaynaklara ve kaynak gruplarına uygulayabileceğiniz ad değeri çifttir.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-142">A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="1c8cb-143">Kaynaklara ve gruplara etiket atadıktan sonra, Get-AzureRmResource ve Get-AzureRmResourceGroup *Etiket parametresini kullanarak* etiket adına veya adlarına göre kaynak ve grupları arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-143">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="1c8cb-144">Kaynaklarınızın veya maliyet merkezinin olduğu gibi kaynaklarınızı sınıflandırmak veya kaynaklarla ilgili notları veya açıklamaları izlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-144">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="1c8cb-145">Etiket eklemek veya değiştirmek için, kaynak grubun etiket koleksiyonunu değiştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-145">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="1c8cb-146">Etiketi silmek için, silmek istediğiniz etiket dışında **Get-AzureRmResourceGroup** kaynağından, şu anda kaynak grubuna uygulanmış olan bir karma tablo girin.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-146">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="1c8cb-147">Kaynak grubundaki tüm etiketleri silmek için boş bir karma tablo belirtin: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="1c8cb-147">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c8cb-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c8cb-148">-DefaultProfile</span></span>
<span data-ttu-id="1c8cb-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c8cb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8cb-150">CommonParameters</span></span>
<span data-ttu-id="1c8cb-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c8cb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8cb-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c8cb-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8cb-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c8cb-153">INPUTS</span></span>

### <span data-ttu-id="1c8cb-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1c8cb-154">None</span></span>

## <span data-ttu-id="1c8cb-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c8cb-155">OUTPUTS</span></span>

### <span data-ttu-id="1c8cb-156">Microsoft. Azure. Commands. resources. modeller. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c8cb-156">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="1c8cb-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c8cb-157">NOTES</span></span>

## <span data-ttu-id="1c8cb-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c8cb-158">RELATED LINKS</span></span>

[<span data-ttu-id="1c8cb-159">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1c8cb-159">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="1c8cb-160">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c8cb-160">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="1c8cb-161">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c8cb-161">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="1c8cb-162">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c8cb-162">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
