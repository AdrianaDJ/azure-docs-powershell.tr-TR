---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: 7264733055322c3d5886ff57f50d22e23f932a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762288"
---
# <span data-ttu-id="fbe6f-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fbe6f-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="fbe6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe6f-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe6f-103">Bir Azure Kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbe6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbe6f-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe6f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbe6f-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe6f-106">**Yeni-AzureRmResourceGroup** cmdlet 'ı bir Azure Kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="fbe6f-107">Yalnızca bir ad ve konum kullanarak bir kaynak grubu oluşturabilir ve ardından kaynak grubuna eklemek üzere kaynak oluşturmak için New-AzureRmResource cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="fbe6f-108">Var olan bir kaynak grubuna dağıtım eklemek için New-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="fbe6f-109">Var olan kaynak grubuna kaynak eklemek için, **New-AzureRmResource** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="fbe6f-110">Azure kaynağı, veritabanı sunucusu, veritabanı veya Web sitesi gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="fbe6f-111">Bir Azure Kaynak grubu, birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="fbe6f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbe6f-112">EXAMPLES</span></span>

### <span data-ttu-id="fbe6f-113">Örnek 1: boş bir kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="fbe6f-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="fbe6f-114">Bu komut, kaynağı olmayan bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="fbe6f-115">Bu kaynak grubuna kaynak ve dağıtım eklemek için **New-azurermresource** veya **New-AzureRmResourceGroupDeployment** cmdlet 'lerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="fbe6f-116">Örnek 2: konum parametrelerini kullanarak boş bir kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="fbe6f-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

<span data-ttu-id="fbe6f-117">Bu komut, kaynağı olmayan bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="fbe6f-118">Örnek 3: etiketlerle kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="fbe6f-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="fbe6f-119">Bu komut boş bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-119">This command creates an empty resource group.</span></span> <span data-ttu-id="fbe6f-120">Bu komut, örnek 1 ' deki komutla aynı olur; bunun nedeni kaynak grubuna Etiketler atar.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="fbe6f-121">Boş adlı ilk etiket, kaynağı olmayan kaynak gruplarını belirlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="fbe6f-122">İkinci etiket bölümlendirilir ve bir pazarlama değeri içerir.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="fbe6f-123">Yönetim veya bütçeleme için kaynak gruplarını sınıflandırmak için bu gibi bir etiket kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="fbe6f-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbe6f-124">PARAMETERS</span></span>

### <span data-ttu-id="fbe6f-125">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="fbe6f-125">-ApiVersion</span></span>
<span data-ttu-id="fbe6f-126">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="fbe6f-127">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="fbe6f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe6f-128">-DefaultProfile</span></span>
<span data-ttu-id="fbe6f-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fbe6f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe6f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="fbe6f-130">-Force</span></span>
<span data-ttu-id="fbe6f-131">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fbe6f-132">-Konum</span><span class="sxs-lookup"><span data-stu-id="fbe6f-132">-Location</span></span>
<span data-ttu-id="fbe6f-133">Kaynak grubunun konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="fbe6f-134">Batı ABD veya Güneydoğu Asya gibi bir Azure veri merkezi konumu belirtin.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="fbe6f-135">Herhangi bir konuma kaynak grubu yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-135">You can place a resource group in any location.</span></span> <span data-ttu-id="fbe6f-136">Kaynak grubunun Azure aboneliğinizde aynı konumda veya kaynaklarıyla aynı konumda olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="fbe6f-137">Hangi konumun kaynak türlerini desteklediğini belirlemek için Get-AzureRmResourceProvider cmdlet 'ini *Providernamespace* parametresiyle kullanın.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-137">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe6f-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="fbe6f-138">-Name</span></span>
<span data-ttu-id="fbe6f-139">Kaynak grubu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="fbe6f-140">Kaynak adı abonelikte benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="fbe6f-141">Bu ada sahip bir kaynak grubu zaten varsa, komut varolan kaynak grubunu değiştirmeden önce sizden onay sorar.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe6f-142">-Pre-</span><span class="sxs-lookup"><span data-stu-id="fbe6f-142">-Pre</span></span>
<span data-ttu-id="fbe6f-143">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fbe6f-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fbe6f-144">-Tag</span></span>
<span data-ttu-id="fbe6f-145">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fbe6f-146">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"} etiket eklemek veya değiştirmek Için, kaynak grubunun etiket koleksiyonunu değiştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="fbe6f-147">Kaynaklara ve gruplara etiket atadıktan sonra, Get-AzureRmResource ve Get-AzureRmResourceGroup *Etiket parametresini kullanarak* etiket adına veya ad ve değere göre arama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="fbe6f-148">Kaynaklarınızın veya maliyet merkezinin olduğu gibi kaynaklarınızı sınıflandırmak veya kaynaklarla ilgili notları veya açıklamaları izlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="fbe6f-149">Önceden tanımlanmış etiketleri almak için Get-AzureRMTag cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-149">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe6f-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbe6f-150">-Confirm</span></span>
<span data-ttu-id="fbe6f-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe6f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe6f-152">-WhatIf</span></span>
<span data-ttu-id="fbe6f-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe6f-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe6f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe6f-155">CommonParameters</span></span>
<span data-ttu-id="fbe6f-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbe6f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe6f-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe6f-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe6f-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbe6f-158">INPUTS</span></span>

### <span data-ttu-id="fbe6f-159">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fbe6f-159">None</span></span>

## <span data-ttu-id="fbe6f-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbe6f-160">OUTPUTS</span></span>

### <span data-ttu-id="fbe6f-161">Microsoft. Azure. Commands. ResourceManagement. modeller. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fbe6f-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="fbe6f-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbe6f-162">NOTES</span></span>

## <span data-ttu-id="fbe6f-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbe6f-163">RELATED LINKS</span></span>

[<span data-ttu-id="fbe6f-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="fbe6f-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="fbe6f-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fbe6f-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="fbe6f-166">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fbe6f-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="fbe6f-167">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fbe6f-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="fbe6f-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fbe6f-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="fbe6f-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fbe6f-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
