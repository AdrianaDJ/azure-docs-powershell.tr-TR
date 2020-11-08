---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097196"
---
# <span data-ttu-id="4288c-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4288c-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="4288c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4288c-102">SYNOPSIS</span></span>
<span data-ttu-id="4288c-103">Kaynak grubunda değişiklik yapar.</span><span class="sxs-lookup"><span data-stu-id="4288c-103">Modifies a resource group.</span></span>

## <span data-ttu-id="4288c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4288c-104">SYNTAX</span></span>

### <span data-ttu-id="4288c-105">SetByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4288c-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4288c-106">Setbyresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="4288c-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4288c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4288c-107">DESCRIPTION</span></span>
<span data-ttu-id="4288c-108">**Set-AzResourceGroup** cmdlet 'i, kaynak grubunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4288c-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="4288c-109">Bu cmdlet 'i kaynak grubuna uygulanmış Azure etiketlerini eklemek, değiştirmek veya silmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4288c-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="4288c-110">Etiketleri değiştirmek için kaynak grubunu ve *etiket* parametresini tanımlayacak *ad* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4288c-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="4288c-111">Bu cmdlet 'i kaynak grubunun adını değiştirmek için kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4288c-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="4288c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4288c-112">EXAMPLES</span></span>

### <span data-ttu-id="4288c-113">Örnek 1: kaynak grubuna etiket uygulama</span><span class="sxs-lookup"><span data-stu-id="4288c-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="4288c-114">Bu komut, mevcut etiketleri olmayan bir kaynak grubuna bir değer içeren bir departman etiketi uygular.</span><span class="sxs-lookup"><span data-stu-id="4288c-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="4288c-115">Örnek 2: kaynak grubuna etiket ekleme</span><span class="sxs-lookup"><span data-stu-id="4288c-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="4288c-116">Bu örnek, mevcut etiketleri olan kaynak grubuna onaylanmış bir değer ve bir FY2016 etiketi içeren bir durum etiketi ekler.</span><span class="sxs-lookup"><span data-stu-id="4288c-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="4288c-117">Belirttiğiniz Etiketler var olan etiketlerin yerine, varolan etiketleri yeni etiket koleksiyonuna eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4288c-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="4288c-118">İlk komut ContosoRG kaynak grubunu alır ve etiket yöntemini kullanarak etiketleri özelliğinin değerini alır.</span><span class="sxs-lookup"><span data-stu-id="4288c-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="4288c-119">Komut, etiketleri $Tags değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4288c-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="4288c-120">İkinci komut $Tags değişkeninde etiketleri alır.</span><span class="sxs-lookup"><span data-stu-id="4288c-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="4288c-121">Üçüncü komut, FY2016 ve etiketlerini $Tags değişkeninde etiket dizisine eklemek için + = atama işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4288c-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="4288c-122">Dördüncü komut, $Tags değişkenindeki etiketleri ContosoRG kaynak grubuna uygulamak için **set-AzResourceGroup** *etiket* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4288c-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="4288c-123">Beşinci komut, ContosoRG kaynak grubuna uygulanan tüm etiketleri alır.</span><span class="sxs-lookup"><span data-stu-id="4288c-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="4288c-124">Çıktıda, kaynak grubunda bölüm etiketi ve iki yeni etiket, durum ve FY2015 bulunur.</span><span class="sxs-lookup"><span data-stu-id="4288c-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="4288c-125">Örnek 3: kaynak grubun tüm etiketlerini silme</span><span class="sxs-lookup"><span data-stu-id="4288c-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="4288c-126">Bu komut, ContosoRG kaynak grubundaki tüm etiketleri silmek için boş karma tablo değeri olan *Tag* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4288c-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="4288c-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4288c-127">PARAMETERS</span></span>

### <span data-ttu-id="4288c-128">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="4288c-128">-ApiVersion</span></span>
<span data-ttu-id="4288c-129">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4288c-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4288c-130">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4288c-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4288c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4288c-131">-DefaultProfile</span></span>
<span data-ttu-id="4288c-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4288c-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4288c-133">-ID</span><span class="sxs-lookup"><span data-stu-id="4288c-133">-Id</span></span>
<span data-ttu-id="4288c-134">Değiştirilecek kaynak grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4288c-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4288c-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="4288c-135">-Name</span></span>
<span data-ttu-id="4288c-136">Değiştirilecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4288c-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4288c-137">-Pre-</span><span class="sxs-lookup"><span data-stu-id="4288c-137">-Pre</span></span>
<span data-ttu-id="4288c-138">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4288c-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4288c-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4288c-139">-Tag</span></span>
<span data-ttu-id="4288c-140">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4288c-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4288c-141">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"} etiket, kaynak ve kaynak gruplarına oluşturabileceğiniz ve uygulayabileceğiniz ad-değer çiftidir.</span><span class="sxs-lookup"><span data-stu-id="4288c-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="4288c-142">Kaynaklara ve gruplara etiket atadıktan sonra, Get-AzResource ve Get-AzResourceGroup *Etiket parametresini kullanarak* etiket adına veya adlarına göre kaynak ve grupları arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4288c-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="4288c-143">Kaynaklarınızın veya maliyet merkezinin olduğu gibi kaynaklarınızı sınıflandırmak veya kaynaklarla ilgili notları veya açıklamaları izlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4288c-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="4288c-144">Etiket eklemek veya değiştirmek için, kaynak grubun etiket koleksiyonunu değiştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4288c-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="4288c-145">Etiketi silmek için, silmek istediğiniz etiket **dışında, kaynak** grubuna şu anda kaynak grubuna uygulanmış olan tüm etiketlerin bulunduğu bir karma tablo girin.</span><span class="sxs-lookup"><span data-stu-id="4288c-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="4288c-146">Kaynak grubundaki tüm etiketleri silmek için boş bir karma tablo belirtin: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="4288c-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="4288c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4288c-147">CommonParameters</span></span>
<span data-ttu-id="4288c-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4288c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4288c-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4288c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4288c-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4288c-150">INPUTS</span></span>

### <span data-ttu-id="4288c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="4288c-151">System.String</span></span>

### <span data-ttu-id="4288c-152">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4288c-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4288c-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4288c-153">OUTPUTS</span></span>

### <span data-ttu-id="4288c-154">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4288c-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="4288c-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4288c-155">NOTES</span></span>

## <span data-ttu-id="4288c-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4288c-156">RELATED LINKS</span></span>

[<span data-ttu-id="4288c-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="4288c-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="4288c-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4288c-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="4288c-159">Yeni-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4288c-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="4288c-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4288c-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
