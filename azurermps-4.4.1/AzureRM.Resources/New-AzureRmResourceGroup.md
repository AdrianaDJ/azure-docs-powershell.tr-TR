---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: ccb0b4afdf39510461dd0f6627748492ba22818f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590666"
---
# <span data-ttu-id="4d6b3-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d6b3-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="4d6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6b3-103">Bir Azure Kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d6b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d6b3-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d6b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="4d6b3-106">**Yeni-AzureRmResourceGroup** cmdlet 'ı bir Azure Kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>

<span data-ttu-id="4d6b3-107">Yalnızca bir ad ve konum kullanarak bir kaynak grubu oluşturabilir ve ardından kaynak grubuna eklemek üzere kaynak oluşturmak için New-AzureRmResource cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>

<span data-ttu-id="4d6b3-108">Var olan bir kaynak grubuna dağıtım eklemek için New-AzureRmResourceGroupDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="4d6b3-109">Var olan kaynak grubuna kaynak eklemek için, **New-AzureRmResource** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="4d6b3-110">Azure kaynağı, veritabanı sunucusu, veritabanı veya Web sitesi gibi kullanıcı tarafından yönetilen bir Azure varlıksitesidir.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="4d6b3-111">Bir Azure Kaynak grubu, birim olarak dağıtılan bir Azure kaynakları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="4d6b3-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d6b3-112">EXAMPLES</span></span>

### <span data-ttu-id="4d6b3-113">Örnek 1: boş bir kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="4d6b3-113">Example 1: Create an empty resource group</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US"
```

<span data-ttu-id="4d6b3-114">Bu komut, kaynağı olmayan bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="4d6b3-115">Bu kaynak grubuna kaynak ve dağıtım eklemek için **New-azurermresource** veya **New-AzureRmResourceGroupDeployment** cmdlet 'lerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="4d6b3-116">Örnek 2: etiketlerle bir kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="4d6b3-116">Example 2: Create a resource group with tags</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US" -Tag @{"Empty"=$null; "Department"="Marketing"}
```

<span data-ttu-id="4d6b3-117">Bu komut boş bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-117">This command creates an empty resource group.</span></span> <span data-ttu-id="4d6b3-118">Bu komut, örnek 1 ' deki komutla aynı olur; bunun nedeni kaynak grubuna Etiketler atar.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-118">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="4d6b3-119">Boş adlı ilk etiket, kaynağı olmayan kaynak gruplarını belirlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-119">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="4d6b3-120">İkinci etiket bölümlendirilir ve bir pazarlama değeri içerir.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-120">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="4d6b3-121">Yönetim veya bütçeleme için kaynak gruplarını sınıflandırmak için bu gibi bir etiket kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-121">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="4d6b3-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d6b3-122">PARAMETERS</span></span>

### <span data-ttu-id="4d6b3-123">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="4d6b3-123">-ApiVersion</span></span>
<span data-ttu-id="4d6b3-124">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4d6b3-125">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4d6b3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4d6b3-126">-Force</span></span>
<span data-ttu-id="4d6b3-127">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d6b3-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="4d6b3-128">-Location</span></span>
<span data-ttu-id="4d6b3-129">Kaynak grubunun konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-129">Specifies the location of the resource group.</span></span> <span data-ttu-id="4d6b3-130">Batı ABD veya Güneydoğu Asya gibi bir Azure veri merkezi konumu belirtin.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-130">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="4d6b3-131">Herhangi bir konuma kaynak grubu yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-131">You can place a resource group in any location.</span></span> <span data-ttu-id="4d6b3-132">Kaynak grubunun Azure aboneliğinizde aynı konumda veya kaynaklarıyla aynı konumda olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-132">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>

<span data-ttu-id="4d6b3-133">Hangi konumun kaynak türlerini desteklediğini belirlemek için Get-AzureRmResourceProvider cmdlet 'ini *Providernamespace* parametresiyle kullanın.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-133">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="4d6b3-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d6b3-134">-Name</span></span>
<span data-ttu-id="4d6b3-135">Kaynak grubu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-135">Specifies a name for the resource group.</span></span> <span data-ttu-id="4d6b3-136">Kaynak adı abonelikte benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-136">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="4d6b3-137">Bu ada sahip bir kaynak grubu zaten varsa, komut varolan kaynak grubunu değiştirmeden önce sizden onay sorar.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-137">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="4d6b3-138">-Pre-</span><span class="sxs-lookup"><span data-stu-id="4d6b3-138">-Pre</span></span>
<span data-ttu-id="4d6b3-139">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4d6b3-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4d6b3-140">-Tag</span></span>
<span data-ttu-id="4d6b3-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4d6b3-142">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4d6b3-142">For example:</span></span>

<span data-ttu-id="4d6b3-143">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="4d6b3-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="4d6b3-144">Etiket eklemek veya değiştirmek için, kaynak grubun etiket koleksiyonunu değiştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span>

<span data-ttu-id="4d6b3-145">Kaynaklara ve gruplara etiket atadıktan sonra, Get-AzureRmResource ve Get-AzureRmResourceGroup *Etiket parametresini kullanarak* etiket adına veya ad ve değere göre arama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-145">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="4d6b3-146">Kaynaklarınızın veya maliyet merkezinin olduğu gibi kaynaklarınızı sınıflandırmak veya kaynaklarla ilgili notları veya açıklamaları izlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-146">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="4d6b3-147">Önceden tanımlanmış etiketleri almak için Get-AzureRMTag cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-147">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="4d6b3-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d6b3-148">-Confirm</span></span>
<span data-ttu-id="4d6b3-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d6b3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d6b3-150">-WhatIf</span></span>
<span data-ttu-id="4d6b3-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d6b3-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d6b3-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d6b3-153">-DefaultProfile</span></span>
<span data-ttu-id="4d6b3-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d6b3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6b3-155">CommonParameters</span></span>
<span data-ttu-id="4d6b3-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d6b3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6b3-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d6b3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6b3-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d6b3-158">INPUTS</span></span>

### <span data-ttu-id="4d6b3-159">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4d6b3-159">None</span></span>

## <span data-ttu-id="4d6b3-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d6b3-160">OUTPUTS</span></span>

### <span data-ttu-id="4d6b3-161">Microsoft. Azure. Commands. ResourceManagement. modeller. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d6b3-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="4d6b3-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d6b3-162">NOTES</span></span>

## <span data-ttu-id="4d6b3-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d6b3-163">RELATED LINKS</span></span>

[<span data-ttu-id="4d6b3-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4d6b3-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="4d6b3-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d6b3-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="4d6b3-166">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="4d6b3-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="4d6b3-167">Yeni-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4d6b3-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="4d6b3-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d6b3-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="4d6b3-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d6b3-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
