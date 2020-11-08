---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: dc619aacd4089ce854eb5d342c2308a38a60cb28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103916"
---
# <span data-ttu-id="39dbe-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39dbe-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="39dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="39dbe-103">Kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="39dbe-103">Gets resource groups.</span></span>

## <span data-ttu-id="39dbe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39dbe-104">SYNTAX</span></span>

### <span data-ttu-id="39dbe-105">GetByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="39dbe-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39dbe-106">Getbyresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="39dbe-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39dbe-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="39dbe-107">DESCRIPTION</span></span>
<span data-ttu-id="39dbe-108">**Get-AzResourceGroup** cmdlet 'i geçerli abonelikteki Azure kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="39dbe-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="39dbe-109">Tüm kaynak gruplarını alabilir veya bir kaynak grubunu ada veya başka özelliklere göre belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="39dbe-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="39dbe-110">Varsayılan olarak, bu cmdlet geçerli abonelikteki tüm kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="39dbe-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="39dbe-111">Azure kaynakları ve Azure Resource Groups hakkında daha fazla bilgi için New-AzResourceGroup cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="39dbe-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="39dbe-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39dbe-112">EXAMPLES</span></span>

### <span data-ttu-id="39dbe-113">Örnek 1: ada göre kaynak grubu alma</span><span class="sxs-lookup"><span data-stu-id="39dbe-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="39dbe-114">Bu komut, Kurerblogu adlı aboneliğinizdeki Azure kaynak grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="39dbe-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="39dbe-115">Örnek 2: kaynak grubunun tüm etiketlerini alma</span><span class="sxs-lookup"><span data-stu-id="39dbe-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="39dbe-116">Bu komut ContosoRG adındaki kaynak grubunu alır ve bu grupla ilişkilendirilmiş etiketleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="39dbe-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="39dbe-117">Örnek 3: konuma göre kaynak gruplarını gösterme</span><span class="sxs-lookup"><span data-stu-id="39dbe-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="39dbe-118">Örnek 4: belirli bir konumdaki tüm kaynak gruplarının adlarını gösterme</span><span class="sxs-lookup"><span data-stu-id="39dbe-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="39dbe-119">Örnek 5: adları WebSunucusu ile başlayan kaynak gruplarını göster</span><span class="sxs-lookup"><span data-stu-id="39dbe-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="39dbe-120">Örnek 6: ada göre kaynak grubu alma</span><span class="sxs-lookup"><span data-stu-id="39dbe-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="39dbe-121">Bu komut aboneliğinizdeki "Engineerblogu" ile başlayan Azure kaynak grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="39dbe-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="39dbe-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39dbe-122">PARAMETERS</span></span>

### <span data-ttu-id="39dbe-123">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="39dbe-123">-ApiVersion</span></span>
<span data-ttu-id="39dbe-124">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="39dbe-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="39dbe-125">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="39dbe-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="39dbe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39dbe-126">-DefaultProfile</span></span>
<span data-ttu-id="39dbe-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="39dbe-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39dbe-128">-ID</span><span class="sxs-lookup"><span data-stu-id="39dbe-128">-Id</span></span>
<span data-ttu-id="39dbe-129">Alınacak kaynak grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="39dbe-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="39dbe-130">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="39dbe-130">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39dbe-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="39dbe-131">-Location</span></span>
<span data-ttu-id="39dbe-132">Alınacak kaynak grubunun konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="39dbe-132">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="39dbe-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="39dbe-133">-Name</span></span>
<span data-ttu-id="39dbe-134">Alınacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39dbe-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="39dbe-135">Bu parametre, dizenin başında ve/veya sonunda joker karakterleri destekler.</span><span class="sxs-lookup"><span data-stu-id="39dbe-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="39dbe-136">-Pre-</span><span class="sxs-lookup"><span data-stu-id="39dbe-136">-Pre</span></span>
<span data-ttu-id="39dbe-137">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="39dbe-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="39dbe-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="39dbe-138">-Tag</span></span>
<span data-ttu-id="39dbe-139">Kaynak gruplarını filtreleme</span><span class="sxs-lookup"><span data-stu-id="39dbe-139">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39dbe-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39dbe-140">CommonParameters</span></span>
<span data-ttu-id="39dbe-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39dbe-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39dbe-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="39dbe-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39dbe-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39dbe-143">INPUTS</span></span>

### <span data-ttu-id="39dbe-144">System. String</span><span class="sxs-lookup"><span data-stu-id="39dbe-144">System.String</span></span>

### <span data-ttu-id="39dbe-145">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="39dbe-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="39dbe-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39dbe-146">OUTPUTS</span></span>

### <span data-ttu-id="39dbe-147">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39dbe-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="39dbe-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39dbe-148">NOTES</span></span>

## <span data-ttu-id="39dbe-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39dbe-149">RELATED LINKS</span></span>

[<span data-ttu-id="39dbe-150">Yeni-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39dbe-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="39dbe-151">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39dbe-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="39dbe-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39dbe-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


