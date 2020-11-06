---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592557"
---
# <span data-ttu-id="020d7-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="020d7-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="020d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="020d7-102">SYNOPSIS</span></span>
<span data-ttu-id="020d7-103">Kaynak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="020d7-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="020d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="020d7-104">SYNTAX</span></span>

### <span data-ttu-id="020d7-105">Ad temelinde kaynak grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="020d7-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="020d7-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="020d7-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="020d7-107">Kimliği temel alan kaynak grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="020d7-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="020d7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="020d7-108">DESCRIPTION</span></span>
<span data-ttu-id="020d7-109">**Remove-AzureRmResourceGroup** cmdlet 'i, bir Azure kaynak grubunu ve kaynaklarını geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="020d7-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="020d7-110">Kaynak grubundan çıkmak için Remove-AzureRmResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="020d7-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="020d7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="020d7-111">EXAMPLES</span></span>

### <span data-ttu-id="020d7-112">Örnek 1: kaynak grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="020d7-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="020d7-113">Bu komut, ContosoRG01 kaynak grubunu abonelikten çıkarır.</span><span class="sxs-lookup"><span data-stu-id="020d7-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="020d7-114">Cmdlet sizden onay ister ve çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="020d7-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="020d7-115">Örnek 2: onaysız kaynak grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="020d7-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="020d7-116">Bu komut, ContosoRG01 kaynak grubunu almak için Get-AzureRmResourceGroup cmdlet 'ini kullanır ve ardından ardışık düzen işlecini kullanarak **-AzureRmResourceGroup öğesini kaldıracak** şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="020d7-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="020d7-117">*Ayrıntılı* ortak parametre işlemle ilgili durum bilgilerini alır ve *Force* parametresi onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="020d7-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="020d7-118">Örnek 3: tüm kaynak gruplarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="020d7-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="020d7-119">Bu komut **Get-azurermresourcegroup** cmdlet 'ini kullanarak tüm kaynak gruplarını alır ve ardından bunları ardışık düzen işlecini kullanarak **-Azurermresourcegroup öğesini kaldıracak** şekilde geçirir.</span><span class="sxs-lookup"><span data-stu-id="020d7-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="020d7-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="020d7-120">PARAMETERS</span></span>

### <span data-ttu-id="020d7-121">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="020d7-121">-ApiVersion</span></span>
<span data-ttu-id="020d7-122">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="020d7-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="020d7-123">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="020d7-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="020d7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="020d7-124">-Force</span></span>
<span data-ttu-id="020d7-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="020d7-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="020d7-126">-ID</span><span class="sxs-lookup"><span data-stu-id="020d7-126">-Id</span></span>
<span data-ttu-id="020d7-127">Kaldırılacak kaynak grubu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="020d7-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="020d7-128">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="020d7-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="020d7-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="020d7-129">-Name</span></span>
<span data-ttu-id="020d7-130">Kaldırılacak kaynak gruplarının adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="020d7-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="020d7-131">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="020d7-131">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="020d7-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="020d7-132">-Pre</span></span>
<span data-ttu-id="020d7-133">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="020d7-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="020d7-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="020d7-134">-Confirm</span></span>
<span data-ttu-id="020d7-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="020d7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="020d7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="020d7-136">-WhatIf</span></span>
<span data-ttu-id="020d7-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="020d7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="020d7-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="020d7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="020d7-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020d7-139">-DefaultProfile</span></span>
<span data-ttu-id="020d7-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="020d7-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="020d7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020d7-141">CommonParameters</span></span>
<span data-ttu-id="020d7-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="020d7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020d7-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="020d7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020d7-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="020d7-144">INPUTS</span></span>

### <span data-ttu-id="020d7-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="020d7-145">None</span></span>

## <span data-ttu-id="020d7-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="020d7-146">OUTPUTS</span></span>

### <span data-ttu-id="020d7-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="020d7-147">None</span></span>

## <span data-ttu-id="020d7-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="020d7-148">NOTES</span></span>

## <span data-ttu-id="020d7-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="020d7-149">RELATED LINKS</span></span>

[<span data-ttu-id="020d7-150">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="020d7-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="020d7-151">Yeni-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="020d7-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="020d7-152">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="020d7-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


