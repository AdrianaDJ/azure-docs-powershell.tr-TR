---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763333"
---
# <span data-ttu-id="8b48e-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b48e-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="8b48e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b48e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b48e-103">Kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="8b48e-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b48e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b48e-104">SYNTAX</span></span>

### <span data-ttu-id="8b48e-105">Ad temelinde kaynak grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="8b48e-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="8b48e-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="8b48e-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b48e-107">Kimliği temel alan kaynak grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="8b48e-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b48e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b48e-108">DESCRIPTION</span></span>
<span data-ttu-id="8b48e-109">**Get-AzureRmResourceGroup** cmdlet 'i geçerli abonelikteki Azure kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="8b48e-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="8b48e-110">Tüm kaynak gruplarını alabilir veya bir kaynak grubunu ada veya başka özelliklere göre belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b48e-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="8b48e-111">Varsayılan olarak, bu cmdlet geçerli abonelikteki tüm kaynak gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="8b48e-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="8b48e-112">Azure kaynakları ve Azure Resource Groups hakkında daha fazla bilgi için New-AzureRmResourceGroup cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="8b48e-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="8b48e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b48e-113">EXAMPLES</span></span>

### <span data-ttu-id="8b48e-114">Örnek 1: ada göre kaynak grubu alma</span><span class="sxs-lookup"><span data-stu-id="8b48e-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="8b48e-115">Bu komut, Kurerblogu adlı aboneliğinizdeki Azure kaynak grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="8b48e-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="8b48e-116">Örnek 2: kaynak grubunun tüm etiketlerini alma</span><span class="sxs-lookup"><span data-stu-id="8b48e-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="8b48e-117">Bu komut ContosoRG adındaki kaynak grubunu alır ve bu grupla ilişkilendirilmiş etiketleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="8b48e-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="8b48e-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b48e-118">PARAMETERS</span></span>

### <span data-ttu-id="8b48e-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="8b48e-119">-ApiVersion</span></span>
<span data-ttu-id="8b48e-120">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b48e-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8b48e-121">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b48e-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8b48e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="8b48e-122">-Id</span></span>
<span data-ttu-id="8b48e-123">Alınacak kaynak grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b48e-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="8b48e-124">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8b48e-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b48e-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="8b48e-125">-Location</span></span>
<span data-ttu-id="8b48e-126">Alınacak kaynak grubunun konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b48e-126">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b48e-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b48e-127">-Name</span></span>
<span data-ttu-id="8b48e-128">Alınacak kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b48e-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="8b48e-129">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8b48e-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b48e-130">-Pre-</span><span class="sxs-lookup"><span data-stu-id="8b48e-130">-Pre</span></span>
<span data-ttu-id="8b48e-131">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b48e-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8b48e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b48e-132">-DefaultProfile</span></span>
<span data-ttu-id="8b48e-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b48e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b48e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b48e-134">CommonParameters</span></span>
<span data-ttu-id="8b48e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b48e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b48e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b48e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b48e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b48e-137">INPUTS</span></span>

### <span data-ttu-id="8b48e-138">Dizisi</span><span class="sxs-lookup"><span data-stu-id="8b48e-138">String</span></span>
<span data-ttu-id="8b48e-139">Girişi cmdlet 'e, özellik adı ile, ancak değere göre kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="8b48e-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="8b48e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b48e-140">OUTPUTS</span></span>

### <span data-ttu-id="8b48e-141">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b48e-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="8b48e-142">Bu cmdlet kaynak gruplarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b48e-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="8b48e-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b48e-143">NOTES</span></span>

## <span data-ttu-id="8b48e-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b48e-144">RELATED LINKS</span></span>

[<span data-ttu-id="8b48e-145">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b48e-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="8b48e-146">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b48e-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="8b48e-147">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b48e-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


