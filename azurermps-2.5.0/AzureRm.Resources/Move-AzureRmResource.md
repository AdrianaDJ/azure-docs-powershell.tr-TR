---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
ms.openlocfilehash: 4f50aea600fe930de62a65d566b6a6ec723fc8de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939675"
---
# <span data-ttu-id="fa18b-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fa18b-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="fa18b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa18b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa18b-103">Kaynağı farklı bir kaynak grubuna veya aboneliğe taşıma.</span><span class="sxs-lookup"><span data-stu-id="fa18b-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa18b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa18b-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa18b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa18b-105">DESCRIPTION</span></span>
<span data-ttu-id="fa18b-106">**Taşıma-AzureRmResource** cmdlet 'i, var olan kaynakları farklı bir kaynak grubuna taşır.</span><span class="sxs-lookup"><span data-stu-id="fa18b-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="fa18b-107">Bu kaynak grubu farklı bir abonelikte olabilir.</span><span class="sxs-lookup"><span data-stu-id="fa18b-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="fa18b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa18b-108">EXAMPLES</span></span>

### <span data-ttu-id="fa18b-109">Örnek 1: kaynağı kaynak grubuna taşıma</span><span class="sxs-lookup"><span data-stu-id="fa18b-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="fa18b-110">İlk komut, Get-AzureRmResource cmdlet 'ini kullanarak ContosoStorageAccount adlı bir kaynak alır ve bu kaynağı $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fa18b-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="fa18b-111">İkinci komut bu kaynağı ResourceGroup14 adlı kaynak grubuna taşır.</span><span class="sxs-lookup"><span data-stu-id="fa18b-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="fa18b-112">Komut, $Resource **RESOURCEID** özelliğini kullanarak taşınacak kaynağı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fa18b-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="fa18b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa18b-113">PARAMETERS</span></span>

### <span data-ttu-id="fa18b-114">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="fa18b-114">-ApiVersion</span></span>
<span data-ttu-id="fa18b-115">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18b-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fa18b-116">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="fa18b-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fa18b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa18b-117">-DefaultProfile</span></span>
<span data-ttu-id="fa18b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fa18b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa18b-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa18b-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="fa18b-120">Bu cmdlet 'in kaynakları taşıdıkları kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18b-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="fa18b-121">-Destinationsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="fa18b-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="fa18b-122">Bu cmdlet 'in kaynakları taşıdıkları aboneliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18b-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="fa18b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fa18b-123">-Force</span></span>
<span data-ttu-id="fa18b-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fa18b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa18b-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fa18b-125">-InformationAction</span></span>
<span data-ttu-id="fa18b-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18b-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="fa18b-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fa18b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fa18b-128">'A</span><span class="sxs-lookup"><span data-stu-id="fa18b-128">Continue</span></span>
- <span data-ttu-id="fa18b-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="fa18b-129">Ignore</span></span>
- <span data-ttu-id="fa18b-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fa18b-130">Inquire</span></span>
- <span data-ttu-id="fa18b-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fa18b-131">SilentlyContinue</span></span>
- <span data-ttu-id="fa18b-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fa18b-132">Stop</span></span>
- <span data-ttu-id="fa18b-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fa18b-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa18b-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fa18b-134">-InformationVariable</span></span>
<span data-ttu-id="fa18b-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18b-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa18b-136">-Pre-</span><span class="sxs-lookup"><span data-stu-id="fa18b-136">-Pre</span></span>
<span data-ttu-id="fa18b-137">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa18b-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fa18b-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fa18b-138">-ResourceId</span></span>
<span data-ttu-id="fa18b-139">Bu cmdlet 'in hareket ettiği kaynak kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18b-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="fa18b-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa18b-140">-Confirm</span></span>
<span data-ttu-id="fa18b-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa18b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa18b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa18b-142">-WhatIf</span></span>
<span data-ttu-id="fa18b-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa18b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa18b-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa18b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa18b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa18b-145">CommonParameters</span></span>
<span data-ttu-id="fa18b-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa18b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa18b-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa18b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa18b-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa18b-148">INPUTS</span></span>

## <span data-ttu-id="fa18b-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa18b-149">OUTPUTS</span></span>

## <span data-ttu-id="fa18b-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa18b-150">NOTES</span></span>

## <span data-ttu-id="fa18b-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa18b-151">RELATED LINKS</span></span>



[<span data-ttu-id="fa18b-152">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fa18b-152">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="fa18b-153">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fa18b-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="fa18b-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fa18b-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="fa18b-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fa18b-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


