---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: d14d591ffdc0e20934a0cf758407dc2b4e6e152c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107423"
---
# <span data-ttu-id="3d3ed-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="3d3ed-101">Move-AzResource</span></span>

## <span data-ttu-id="3d3ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d3ed-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3ed-103">Kaynağı farklı bir kaynak grubuna veya aboneliğe taşıma.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="3d3ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d3ed-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d3ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d3ed-105">DESCRIPTION</span></span>
<span data-ttu-id="3d3ed-106">**Taþý-AzResource** cmdlet 'i, varolan kaynakları farklı bir kaynak grubuna taşır.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="3d3ed-107">Bu kaynak grubu farklı bir abonelikte olabilir.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="3d3ed-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d3ed-108">EXAMPLES</span></span>

### <span data-ttu-id="3d3ed-109">Örnek 1: kaynağı kaynak grubuna taşıma</span><span class="sxs-lookup"><span data-stu-id="3d3ed-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="3d3ed-110">İlk komut, Get-AzResource cmdlet 'ini kullanarak ContosoStorageAccount adlı bir kaynak alır ve bu kaynağı $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="3d3ed-111">İkinci komut bu kaynağı ResourceGroup14 adlı kaynak grubuna taşır.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="3d3ed-112">Komut, $Resource **RESOURCEID** özelliğini kullanarak taşınacak kaynağı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="3d3ed-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d3ed-113">PARAMETERS</span></span>

### <span data-ttu-id="3d3ed-114">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="3d3ed-114">-ApiVersion</span></span>
<span data-ttu-id="3d3ed-115">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d3ed-116">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3d3ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3ed-117">-DefaultProfile</span></span>
<span data-ttu-id="3d3ed-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3d3ed-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d3ed-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d3ed-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="3d3ed-120">Bu cmdlet 'in kaynakları taşıdıkları kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3ed-121">-Destinationsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="3d3ed-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="3d3ed-122">Bu cmdlet 'in kaynakları taşıdıkları aboneliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3ed-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3d3ed-123">-Force</span></span>
<span data-ttu-id="3d3ed-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d3ed-125">-Pre-</span><span class="sxs-lookup"><span data-stu-id="3d3ed-125">-Pre</span></span>
<span data-ttu-id="3d3ed-126">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3d3ed-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3d3ed-127">-ResourceId</span></span>
<span data-ttu-id="3d3ed-128">Bu cmdlet 'in hareket ettiği kaynak kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3ed-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d3ed-129">-Confirm</span></span>
<span data-ttu-id="3d3ed-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d3ed-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d3ed-131">-WhatIf</span></span>
<span data-ttu-id="3d3ed-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d3ed-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d3ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3ed-134">CommonParameters</span></span>
<span data-ttu-id="3d3ed-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3ed-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d3ed-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3ed-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d3ed-137">INPUTS</span></span>

### <span data-ttu-id="3d3ed-138">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="3d3ed-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3d3ed-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="3d3ed-139">System.String[]</span></span>

## <span data-ttu-id="3d3ed-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d3ed-140">OUTPUTS</span></span>

### <span data-ttu-id="3d3ed-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d3ed-141">System.Boolean</span></span>

## <span data-ttu-id="3d3ed-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d3ed-142">NOTES</span></span>

## <span data-ttu-id="3d3ed-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d3ed-143">RELATED LINKS</span></span>

[<span data-ttu-id="3d3ed-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="3d3ed-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="3d3ed-145">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="3d3ed-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="3d3ed-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="3d3ed-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="3d3ed-147">Set-Azkaynak</span><span class="sxs-lookup"><span data-stu-id="3d3ed-147">Set-AzResource</span></span>](./Set-AzResource.md)


