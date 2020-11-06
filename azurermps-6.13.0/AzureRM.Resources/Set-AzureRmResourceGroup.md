---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: 4ba57d1f8e1abe8c506f1bcd6625a7a90551f164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593896"
---
# <span data-ttu-id="5cf10-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5cf10-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="5cf10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cf10-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf10-103">Kaynak grubunda değişiklik yapar.</span><span class="sxs-lookup"><span data-stu-id="5cf10-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cf10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cf10-104">SYNTAX</span></span>

### <span data-ttu-id="5cf10-105">SetByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5cf10-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cf10-106">Setbyresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="5cf10-106">SetByResourceGroupId</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cf10-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cf10-107">DESCRIPTION</span></span>
<span data-ttu-id="5cf10-108">**Set-AzureRmResourceGroup** cmdlet 'i, kaynak grubunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5cf10-108">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="5cf10-109">Bu cmdlet 'i kaynak grubuna uygulanmış Azure etiketlerini eklemek, değiştirmek veya silmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cf10-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="5cf10-110">Etiketleri değiştirmek için kaynak grubunu ve *etiket* parametresini tanımlayacak *ad* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5cf10-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="5cf10-111">Bu cmdlet 'i kaynak grubunun adını değiştirmek için kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="5cf10-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="5cf10-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cf10-112">EXAMPLES</span></span>

### <span data-ttu-id="5cf10-113">Örnek 1: kaynak grubuna etiket uygulama</span><span class="sxs-lookup"><span data-stu-id="5cf10-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="5cf10-114">Bu komut, mevcut etiketleri olmayan bir kaynak grubuna bir değer içeren bir departman etiketi uygular.</span><span class="sxs-lookup"><span data-stu-id="5cf10-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="5cf10-115">Örnek 2: kaynak grubuna etiket ekleme</span><span class="sxs-lookup"><span data-stu-id="5cf10-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="5cf10-116">Bu örnek, mevcut etiketleri olan kaynak grubuna onaylanmış bir değer ve bir FY2016 etiketi içeren bir durum etiketi ekler.</span><span class="sxs-lookup"><span data-stu-id="5cf10-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="5cf10-117">Belirttiğiniz Etiketler var olan etiketlerin yerine, varolan etiketleri yeni etiket koleksiyonuna eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5cf10-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="5cf10-118">İlk komut ContosoRG kaynak grubunu alır ve etiket yöntemini kullanarak etiketleri özelliğinin değerini alır.</span><span class="sxs-lookup"><span data-stu-id="5cf10-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="5cf10-119">Komut, etiketleri $Tags değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5cf10-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="5cf10-120">İkinci komut $Tags değişkeninde etiketleri alır.</span><span class="sxs-lookup"><span data-stu-id="5cf10-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="5cf10-121">Üçüncü komut, FY2016 ve etiketlerini $Tags değişkeninde etiket dizisine eklemek için + = atama işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5cf10-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="5cf10-122">Dördüncü komut, ContosoRG kaynak grubuna $Tags değişkeninde etiketleri uygulamak için **set-AzureRmResourceGroup** *etiket* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5cf10-122">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="5cf10-123">Beşinci komut, ContosoRG kaynak grubuna uygulanan tüm etiketleri alır.</span><span class="sxs-lookup"><span data-stu-id="5cf10-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="5cf10-124">Çıktıda, kaynak grubunda bölüm etiketi ve iki yeni etiket, durum ve FY2015 bulunur.</span><span class="sxs-lookup"><span data-stu-id="5cf10-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="5cf10-125">Örnek 3: kaynak grubun tüm etiketlerini silme</span><span class="sxs-lookup"><span data-stu-id="5cf10-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="5cf10-126">Bu komut, ContosoRG kaynak grubundaki tüm etiketleri silmek için boş karma tablo değeri olan *Tag* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf10-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="5cf10-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cf10-127">PARAMETERS</span></span>

### <span data-ttu-id="5cf10-128">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="5cf10-128">-ApiVersion</span></span>
<span data-ttu-id="5cf10-129">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf10-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5cf10-130">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cf10-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5cf10-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf10-131">-DefaultProfile</span></span>
<span data-ttu-id="5cf10-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5cf10-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cf10-133">-ID</span><span class="sxs-lookup"><span data-stu-id="5cf10-133">-Id</span></span>
<span data-ttu-id="5cf10-134">Değiştirilecek kaynak grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf10-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf10-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="5cf10-135">-Name</span></span>
<span data-ttu-id="5cf10-136">Değiştirilecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf10-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf10-137">-Pre-</span><span class="sxs-lookup"><span data-stu-id="5cf10-137">-Pre</span></span>
<span data-ttu-id="5cf10-138">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cf10-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5cf10-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5cf10-139">-Tag</span></span>
<span data-ttu-id="5cf10-140">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="5cf10-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5cf10-141">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"} etiket, kaynak ve kaynak gruplarına oluşturabileceğiniz ve uygulayabileceğiniz ad-değer çiftidir.</span><span class="sxs-lookup"><span data-stu-id="5cf10-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="5cf10-142">Kaynaklara ve gruplara etiket atadıktan sonra, Get-AzureRmResource ve Get-AzureRmResourceGroup *Etiket parametresini kullanarak* etiket adına veya adlarına göre kaynak ve grupları arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cf10-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="5cf10-143">Kaynaklarınızın veya maliyet merkezinin olduğu gibi kaynaklarınızı sınıflandırmak veya kaynaklarla ilgili notları veya açıklamaları izlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cf10-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="5cf10-144">Etiket eklemek veya değiştirmek için, kaynak grubun etiket koleksiyonunu değiştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="5cf10-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="5cf10-145">Etiketi silmek için, silmek istediğiniz etiket dışında **Get-AzureRmResourceGroup** kaynağından, şu anda kaynak grubuna uygulanmış olan bir karma tablo girin.</span><span class="sxs-lookup"><span data-stu-id="5cf10-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="5cf10-146">Kaynak grubundaki tüm etiketleri silmek için boş bir karma tablo belirtin: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="5cf10-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="5cf10-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf10-147">CommonParameters</span></span>
<span data-ttu-id="5cf10-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cf10-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf10-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf10-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf10-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cf10-150">INPUTS</span></span>

### <span data-ttu-id="5cf10-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5cf10-151">None</span></span>

## <span data-ttu-id="5cf10-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cf10-152">OUTPUTS</span></span>

### <span data-ttu-id="5cf10-153">Microsoft. Azure. Commands. resources. modeller. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5cf10-153">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="5cf10-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cf10-154">NOTES</span></span>

## <span data-ttu-id="5cf10-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cf10-155">RELATED LINKS</span></span>

[<span data-ttu-id="5cf10-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5cf10-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="5cf10-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5cf10-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="5cf10-158">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5cf10-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="5cf10-159">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5cf10-159">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
