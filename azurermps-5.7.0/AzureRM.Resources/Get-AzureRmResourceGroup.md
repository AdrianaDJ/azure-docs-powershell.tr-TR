---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: f3924115d68d7e844503e076a214c95bf3d2239d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593443"
---
# <span data-ttu-id="dac4e-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dac4e-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="dac4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dac4e-102">SYNOPSIS</span></span>
<span data-ttu-id="dac4e-103">Kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="dac4e-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dac4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dac4e-104">SYNTAX</span></span>

### <span data-ttu-id="dac4e-105">GetByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dac4e-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dac4e-106">Getbyresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="dac4e-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dac4e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dac4e-107">DESCRIPTION</span></span>
<span data-ttu-id="dac4e-108">**Get-AzureRmResourceGroup** cmdlet 'i geçerli abonelikteki Azure kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="dac4e-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="dac4e-109">Tüm kaynak gruplarını alabilir veya bir kaynak grubunu ada veya başka özelliklere göre belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dac4e-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="dac4e-110">Varsayılan olarak, bu cmdlet geçerli abonelikteki tüm kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="dac4e-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="dac4e-111">Azure kaynakları ve Azure Resource Groups hakkında daha fazla bilgi için New-AzureRmResourceGroup cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="dac4e-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="dac4e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dac4e-112">EXAMPLES</span></span>

### <span data-ttu-id="dac4e-113">Örnek 1: ada göre kaynak grubu alma</span><span class="sxs-lookup"><span data-stu-id="dac4e-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="dac4e-114">Bu komut, Kurerblogu adlı aboneliğinizdeki Azure kaynak grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="dac4e-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="dac4e-115">Örnek 2: kaynak grubunun tüm etiketlerini alma</span><span class="sxs-lookup"><span data-stu-id="dac4e-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="dac4e-116">Bu komut ContosoRG adındaki kaynak grubunu alır ve bu grupla ilişkilendirilmiş etiketleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="dac4e-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="dac4e-117">Örnek 3: konuma göre kaynak gruplarını gösterme</span><span class="sxs-lookup"><span data-stu-id="dac4e-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="dac4e-118">Örnek 4: belirli bir konumdaki tüm kaynak gruplarının adlarını gösterme</span><span class="sxs-lookup"><span data-stu-id="dac4e-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="dac4e-119">Örnek 5: adları WebSunucusu ile başlayan kaynak gruplarını göster</span><span class="sxs-lookup"><span data-stu-id="dac4e-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="dac4e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dac4e-120">PARAMETERS</span></span>

### <span data-ttu-id="dac4e-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="dac4e-121">-ApiVersion</span></span>
<span data-ttu-id="dac4e-122">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac4e-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="dac4e-123">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dac4e-123">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac4e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac4e-124">-DefaultProfile</span></span>
<span data-ttu-id="dac4e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dac4e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac4e-126">-ID</span><span class="sxs-lookup"><span data-stu-id="dac4e-126">-Id</span></span>
<span data-ttu-id="dac4e-127">Alınacak kaynak grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac4e-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="dac4e-128">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="dac4e-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac4e-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="dac4e-129">-Location</span></span>
<span data-ttu-id="dac4e-130">Alınacak kaynak grubunun konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac4e-130">Specifies the location of the resource group to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac4e-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="dac4e-131">-Name</span></span>
<span data-ttu-id="dac4e-132">Alınacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac4e-132">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="dac4e-133">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="dac4e-133">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac4e-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="dac4e-134">-Pre</span></span>
<span data-ttu-id="dac4e-135">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="dac4e-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac4e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac4e-136">CommonParameters</span></span>
<span data-ttu-id="dac4e-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dac4e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac4e-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dac4e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac4e-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dac4e-139">INPUTS</span></span>

### <span data-ttu-id="dac4e-140">Dizisi</span><span class="sxs-lookup"><span data-stu-id="dac4e-140">String</span></span>
<span data-ttu-id="dac4e-141">Girişi cmdlet 'e, özellik adı ile, ancak değere göre kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="dac4e-141">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="dac4e-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dac4e-142">OUTPUTS</span></span>

### <span data-ttu-id="dac4e-143">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dac4e-143">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="dac4e-144">Bu cmdlet kaynak gruplarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="dac4e-144">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="dac4e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dac4e-145">NOTES</span></span>

## <span data-ttu-id="dac4e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dac4e-146">RELATED LINKS</span></span>

[<span data-ttu-id="dac4e-147">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dac4e-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="dac4e-148">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dac4e-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="dac4e-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dac4e-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


