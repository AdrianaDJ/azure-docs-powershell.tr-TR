---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: ce028e52d893372f4a668a278466d4cdc51655f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591621"
---
# <span data-ttu-id="b1c69-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1c69-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="b1c69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1c69-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c69-103">Kaynak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b1c69-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1c69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1c69-104">SYNTAX</span></span>

### <span data-ttu-id="b1c69-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b1c69-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c69-106">Removebyresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="b1c69-106">RemoveByResourceGroupId</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1c69-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1c69-107">DESCRIPTION</span></span>
<span data-ttu-id="b1c69-108">**Remove-AzureRmResourceGroup** cmdlet 'i, bir Azure kaynak grubunu ve kaynaklarını geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b1c69-108">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="b1c69-109">Kaynak grubundan çıkmak için Remove-AzureRmResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b1c69-109">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="b1c69-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1c69-110">EXAMPLES</span></span>

### <span data-ttu-id="b1c69-111">Örnek 1: kaynak grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="b1c69-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="b1c69-112">Bu komut, ContosoRG01 kaynak grubunu abonelikten çıkarır.</span><span class="sxs-lookup"><span data-stu-id="b1c69-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="b1c69-113">Cmdlet sizden onay ister ve çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="b1c69-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="b1c69-114">Örnek 2: onaysız kaynak grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="b1c69-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="b1c69-115">Bu komut, ContosoRG01 kaynak grubunu almak için Get-AzureRmResourceGroup cmdlet 'ini kullanır ve ardından ardışık düzen işlecini kullanarak **-AzureRmResourceGroup öğesini kaldıracak** şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="b1c69-115">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="b1c69-116">*Ayrıntılı* ortak parametre işlemle ilgili durum bilgilerini alır ve *Force* parametresi onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="b1c69-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="b1c69-117">Örnek 3: tüm kaynak gruplarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b1c69-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="b1c69-118">Bu komut **Get-azurermresourcegroup** cmdlet 'ini kullanarak tüm kaynak gruplarını alır ve ardından bunları ardışık düzen işlecini kullanarak **-Azurermresourcegroup öğesini kaldıracak** şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="b1c69-118">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="b1c69-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1c69-119">PARAMETERS</span></span>

### <span data-ttu-id="b1c69-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="b1c69-120">-ApiVersion</span></span>
<span data-ttu-id="b1c69-121">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1c69-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b1c69-122">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1c69-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b1c69-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="b1c69-123">-AsJob</span></span>
<span data-ttu-id="b1c69-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b1c69-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1c69-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c69-125">-DefaultProfile</span></span>
<span data-ttu-id="b1c69-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b1c69-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1c69-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b1c69-127">-Force</span></span>
<span data-ttu-id="b1c69-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b1c69-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1c69-129">-ID</span><span class="sxs-lookup"><span data-stu-id="b1c69-129">-Id</span></span>
<span data-ttu-id="b1c69-130">Kaldırılacak kaynak grubu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1c69-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="b1c69-131">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b1c69-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c69-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1c69-132">-Name</span></span>
<span data-ttu-id="b1c69-133">Kaldırılacak kaynak gruplarının adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1c69-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="b1c69-134">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b1c69-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c69-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="b1c69-135">-Pre</span></span>
<span data-ttu-id="b1c69-136">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1c69-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b1c69-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1c69-137">-Confirm</span></span>
<span data-ttu-id="b1c69-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1c69-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c69-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c69-139">-WhatIf</span></span>
<span data-ttu-id="b1c69-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1c69-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c69-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1c69-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c69-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c69-142">CommonParameters</span></span>
<span data-ttu-id="b1c69-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1c69-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c69-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1c69-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c69-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1c69-145">INPUTS</span></span>

### <span data-ttu-id="b1c69-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b1c69-146">None</span></span>

## <span data-ttu-id="b1c69-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1c69-147">OUTPUTS</span></span>

### <span data-ttu-id="b1c69-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b1c69-148">None</span></span>

## <span data-ttu-id="b1c69-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1c69-149">NOTES</span></span>

## <span data-ttu-id="b1c69-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1c69-150">RELATED LINKS</span></span>

[<span data-ttu-id="b1c69-151">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1c69-151">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="b1c69-152">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1c69-152">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="b1c69-153">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1c69-153">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


