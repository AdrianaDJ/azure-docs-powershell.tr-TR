---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 4f21ce7a14873d201fa18f45c96d508dcd38cb8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274677"
---
# <span data-ttu-id="c314d-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="c314d-101">Move-AzResource</span></span>

## <span data-ttu-id="c314d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c314d-102">SYNOPSIS</span></span>
<span data-ttu-id="c314d-103">Kaynağı farklı bir kaynak grubuna veya aboneliğe taşıma.</span><span class="sxs-lookup"><span data-stu-id="c314d-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="c314d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c314d-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c314d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c314d-105">DESCRIPTION</span></span>
<span data-ttu-id="c314d-106">**Taþý-AzResource** cmdlet 'i, varolan kaynakları farklı bir kaynak grubuna taşır.</span><span class="sxs-lookup"><span data-stu-id="c314d-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="c314d-107">Bu kaynak grubu farklı bir abonelikte olabilir.</span><span class="sxs-lookup"><span data-stu-id="c314d-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="c314d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c314d-108">EXAMPLES</span></span>

### <span data-ttu-id="c314d-109">Örnek 1: kaynağı kaynak grubuna taşıma</span><span class="sxs-lookup"><span data-stu-id="c314d-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="c314d-110">İlk komut, Get-AzResource cmdlet 'ini kullanarak ContosoStorageAccount adlı bir kaynak alır ve bu kaynağı $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c314d-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="c314d-111">İkinci komut bu kaynağı ResourceGroup14 adlı kaynak grubuna taşır.</span><span class="sxs-lookup"><span data-stu-id="c314d-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="c314d-112">Komut, $Resource **RESOURCEID** özelliğini kullanarak taşınacak kaynağı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c314d-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="c314d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c314d-113">PARAMETERS</span></span>

### <span data-ttu-id="c314d-114">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c314d-114">-ApiVersion</span></span>
<span data-ttu-id="c314d-115">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c314d-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c314d-116">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c314d-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c314d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c314d-117">-DefaultProfile</span></span>
<span data-ttu-id="c314d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c314d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c314d-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c314d-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="c314d-120">Bu cmdlet 'in kaynakları taşıdıkları kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c314d-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="c314d-121">-Destinationsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="c314d-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="c314d-122">Bu cmdlet 'in kaynakları taşıdıkları aboneliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c314d-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="c314d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c314d-123">-Force</span></span>
<span data-ttu-id="c314d-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c314d-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c314d-125">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c314d-125">-Pre</span></span>
<span data-ttu-id="c314d-126">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c314d-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c314d-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c314d-127">-ResourceId</span></span>
<span data-ttu-id="c314d-128">Bu cmdlet 'in hareket ettiği kaynak kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c314d-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="c314d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="c314d-129">-Confirm</span></span>
<span data-ttu-id="c314d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c314d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c314d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c314d-131">-WhatIf</span></span>
<span data-ttu-id="c314d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c314d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c314d-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c314d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c314d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c314d-134">CommonParameters</span></span>
<span data-ttu-id="c314d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c314d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c314d-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c314d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c314d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c314d-137">INPUTS</span></span>

### <span data-ttu-id="c314d-138">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="c314d-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c314d-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="c314d-139">System.String[]</span></span>

## <span data-ttu-id="c314d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c314d-140">OUTPUTS</span></span>

### <span data-ttu-id="c314d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c314d-141">System.Boolean</span></span>

## <span data-ttu-id="c314d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c314d-142">NOTES</span></span>

## <span data-ttu-id="c314d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c314d-143">RELATED LINKS</span></span>

[<span data-ttu-id="c314d-144">Find-AzResource</span><span class="sxs-lookup"><span data-stu-id="c314d-144">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="c314d-145">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="c314d-145">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="c314d-146">Yeni-aza kaynağı</span><span class="sxs-lookup"><span data-stu-id="c314d-146">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="c314d-147">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="c314d-147">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="c314d-148">Set-Azkaynak</span><span class="sxs-lookup"><span data-stu-id="c314d-148">Set-AzResource</span></span>](./Set-AzResource.md)


