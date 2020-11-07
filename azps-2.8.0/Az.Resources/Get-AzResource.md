---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 451d70b899f2cb580e23751f6662cd300c301942
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93940228"
---
# <span data-ttu-id="8cdab-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8cdab-101">Get-AzResource</span></span>

## <span data-ttu-id="8cdab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cdab-102">SYNOPSIS</span></span>

<span data-ttu-id="8cdab-103">Kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-103">Gets resources.</span></span>

## <span data-ttu-id="8cdab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8cdab-104">SYNTAX</span></span>

### <span data-ttu-id="8cdab-105">ByTagNameValueParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8cdab-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cdab-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="8cdab-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cdab-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cdab-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cdab-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8cdab-108">DESCRIPTION</span></span>

<span data-ttu-id="8cdab-109">**Get-AzResource** cmdlet 'i Azure kaynaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="8cdab-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8cdab-110">EXAMPLES</span></span>

### <span data-ttu-id="8cdab-111">Örnek 1: geçerli abonelikteki tüm kaynakları alma</span><span class="sxs-lookup"><span data-stu-id="8cdab-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="8cdab-112">Bu komut, geçerli abonelikteki tüm kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="8cdab-113">Örnek 2: kaynak grubundaki tüm kaynakları alma</span><span class="sxs-lookup"><span data-stu-id="8cdab-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="8cdab-114">Bu komut, "testRG" kaynak grubundaki tüm kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="8cdab-115">Örnek 3: kaynak grubu sağlanan joker karakterle eşleşen tüm kaynakları alma</span><span class="sxs-lookup"><span data-stu-id="8cdab-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="8cdab-116">Bu komut, kaynak grubuna "diğer" ile sahip oldukları tüm kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="8cdab-117">Örnek 4: verilen ada sahip tüm kaynakları alma</span><span class="sxs-lookup"><span data-stu-id="8cdab-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="8cdab-118">Bu komut, kaynak adı "testVM" olan tüm kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="8cdab-119">Örnek 5: adı sağlanan joker karakterle eşleşen tüm kaynakları alma</span><span class="sxs-lookup"><span data-stu-id="8cdab-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="8cdab-120">Bu komut, kaynak adı "test" ile başlayan tüm kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="8cdab-121">Örnek 6: verilen kaynak türündeki tüm kaynakları alma</span><span class="sxs-lookup"><span data-stu-id="8cdab-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="8cdab-122">Bu komut, geçerli aboneliklerde sanal makine olan tüm kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="8cdab-123">Örnek 7: kaynak kimliğiyle kaynak alma</span><span class="sxs-lookup"><span data-stu-id="8cdab-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="8cdab-124">Bu komut, "testRG" kaynak grubunda "testVM" adlı bir sanal makine olan sağlanan kaynak kimliğine sahip kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="8cdab-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8cdab-125">PARAMETERS</span></span>

### <span data-ttu-id="8cdab-126">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8cdab-126">-ApiVersion</span></span>

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

### <span data-ttu-id="8cdab-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cdab-127">-DefaultProfile</span></span>
<span data-ttu-id="8cdab-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8cdab-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cdab-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="8cdab-129">-ExpandProperties</span></span>
<span data-ttu-id="8cdab-130">Belirtildiğinde, kaynağın özelliklerini genişletir.</span><span class="sxs-lookup"><span data-stu-id="8cdab-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="8cdab-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="8cdab-131">-Name</span></span>
<span data-ttu-id="8cdab-132">Alınacak kaynakların adı.</span><span class="sxs-lookup"><span data-stu-id="8cdab-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="8cdab-133">Bu parametre, dizenin başında ve/veya sonunda joker karakterleri destekler.</span><span class="sxs-lookup"><span data-stu-id="8cdab-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8cdab-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8cdab-134">-ODataQuery</span></span>

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

### <span data-ttu-id="8cdab-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="8cdab-135">-Pre</span></span>

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

### <span data-ttu-id="8cdab-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cdab-136">-ResourceGroupName</span></span>
<span data-ttu-id="8cdab-137">Alınan kaynakların ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8cdab-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="8cdab-138">Bu parametre, dizenin başında ve/veya sonunda joker karakterleri destekler.</span><span class="sxs-lookup"><span data-stu-id="8cdab-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8cdab-139">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8cdab-139">-ResourceId</span></span>
<span data-ttu-id="8cdab-140">Aşağıdaki örnekte olduğu gibi tam nitelikli kaynak KIMLIĞINI belirtir `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="8cdab-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdab-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8cdab-141">-ResourceType</span></span>
<span data-ttu-id="8cdab-142">Alınacak kaynakların kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="8cdab-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="8cdab-143">Örneğin, Microsoft. COMPUTE/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="8cdab-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdab-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8cdab-144">-Tag</span></span>

<span data-ttu-id="8cdab-145">Belirtilen Azure etiketine sahip kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8cdab-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="8cdab-146">Ad anahtarı veya ad ve değer anahtarları içeren bir karma tablo girin.</span><span class="sxs-lookup"><span data-stu-id="8cdab-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="8cdab-147">Joker karakterler desteklenmez. "Tag", kaynaklara ve kaynak gruplarına uygulayabileceğiniz ad-değer çiftidir.</span><span class="sxs-lookup"><span data-stu-id="8cdab-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="8cdab-148">Kaynaklarınızın veya maliyet merkezinin olduğu gibi kaynaklarınızı sınıflandırmak veya kaynaklarla ilgili notları veya açıklamaları izlemek için etiketleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="8cdab-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="8cdab-149">Bir kaynağa etiket eklemek için, New-AzResource veya Set-AzResource cmdlet 'lerinin Etiket parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8cdab-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="8cdab-150">Önceden tanımlanmış bir etiket oluşturmak için New-AzTag cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8cdab-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="8cdab-151">Windows PowerShell 'de karma tablolarla ilgili yardım için ' Get-Help about_Hashtables ' öğesini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8cdab-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdab-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="8cdab-152">-TagName</span></span>
<span data-ttu-id="8cdab-153">Alınacak kaynak (lar) etiketindeki anahtar.</span><span class="sxs-lookup"><span data-stu-id="8cdab-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdab-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="8cdab-154">-TagValue</span></span>
<span data-ttu-id="8cdab-155">Alınacak kaynak (lar) etiketindeki değer.</span><span class="sxs-lookup"><span data-stu-id="8cdab-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdab-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdab-156">CommonParameters</span></span>
<span data-ttu-id="8cdab-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8cdab-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdab-158">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8cdab-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdab-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8cdab-159">INPUTS</span></span>

### <span data-ttu-id="8cdab-160">System. String</span><span class="sxs-lookup"><span data-stu-id="8cdab-160">System.String</span></span>

## <span data-ttu-id="8cdab-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8cdab-161">OUTPUTS</span></span>

### <span data-ttu-id="8cdab-162">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResource</span><span class="sxs-lookup"><span data-stu-id="8cdab-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="8cdab-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8cdab-163">NOTES</span></span>

## <span data-ttu-id="8cdab-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8cdab-164">RELATED LINKS</span></span>

[<span data-ttu-id="8cdab-165">Taşı-Azkaynak</span><span class="sxs-lookup"><span data-stu-id="8cdab-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="8cdab-166">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="8cdab-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="8cdab-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="8cdab-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="8cdab-168">Set-Azkaynak</span><span class="sxs-lookup"><span data-stu-id="8cdab-168">Set-AzResource</span></span>](./Set-AzResource.md)
