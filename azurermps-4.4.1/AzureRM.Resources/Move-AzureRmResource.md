---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4a40b3fd0045a48d6a69c76970b3835ef2d685c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763329"
---
# <span data-ttu-id="823f1-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="823f1-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="823f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="823f1-102">SYNOPSIS</span></span>
<span data-ttu-id="823f1-103">Kaynağı farklı bir kaynak grubuna veya aboneliğe taşıma.</span><span class="sxs-lookup"><span data-stu-id="823f1-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="823f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="823f1-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="823f1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="823f1-105">DESCRIPTION</span></span>
<span data-ttu-id="823f1-106">**Taşıma-AzureRmResource** cmdlet 'i, var olan kaynakları farklı bir kaynak grubuna taşır.</span><span class="sxs-lookup"><span data-stu-id="823f1-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="823f1-107">Bu kaynak grubu farklı bir abonelikte olabilir.</span><span class="sxs-lookup"><span data-stu-id="823f1-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="823f1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="823f1-108">EXAMPLES</span></span>

### <span data-ttu-id="823f1-109">Örnek 1: kaynağı kaynak grubuna taşıma</span><span class="sxs-lookup"><span data-stu-id="823f1-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="823f1-110">İlk komut, Get-AzureRmResource cmdlet 'ini kullanarak ContosoStorageAccount adlı bir kaynak alır ve bu kaynağı $Resource değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="823f1-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="823f1-111">İkinci komut bu kaynağı ResourceGroup14 adlı kaynak grubuna taşır.</span><span class="sxs-lookup"><span data-stu-id="823f1-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="823f1-112">Komut, $Resource **RESOURCEID** özelliğini kullanarak taşınacak kaynağı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="823f1-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="823f1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="823f1-113">PARAMETERS</span></span>

### <span data-ttu-id="823f1-114">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="823f1-114">-ApiVersion</span></span>
<span data-ttu-id="823f1-115">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="823f1-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="823f1-116">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="823f1-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="823f1-117">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="823f1-117">-DestinationResourceGroupName</span></span>
<span data-ttu-id="823f1-118">Bu cmdlet 'in kaynakları taşıdıkları kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="823f1-118">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="823f1-119">-Destinationsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="823f1-119">-DestinationSubscriptionId</span></span>
<span data-ttu-id="823f1-120">Bu cmdlet 'in kaynakları taşıdıkları aboneliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="823f1-120">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="823f1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="823f1-121">-Force</span></span>
<span data-ttu-id="823f1-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="823f1-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="823f1-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="823f1-123">-InformationAction</span></span>
<span data-ttu-id="823f1-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="823f1-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="823f1-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="823f1-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="823f1-126">'A</span><span class="sxs-lookup"><span data-stu-id="823f1-126">Continue</span></span>
- <span data-ttu-id="823f1-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="823f1-127">Ignore</span></span>
- <span data-ttu-id="823f1-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="823f1-128">Inquire</span></span>
- <span data-ttu-id="823f1-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="823f1-129">SilentlyContinue</span></span>
- <span data-ttu-id="823f1-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="823f1-130">Stop</span></span>
- <span data-ttu-id="823f1-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="823f1-131">Suspend</span></span>

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

### <span data-ttu-id="823f1-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="823f1-132">-InformationVariable</span></span>
<span data-ttu-id="823f1-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="823f1-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="823f1-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="823f1-134">-Pre</span></span>
<span data-ttu-id="823f1-135">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="823f1-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="823f1-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="823f1-136">-ResourceId</span></span>
<span data-ttu-id="823f1-137">Bu cmdlet 'in hareket ettiği kaynak kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="823f1-137">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="823f1-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="823f1-138">-Confirm</span></span>
<span data-ttu-id="823f1-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="823f1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="823f1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="823f1-140">-WhatIf</span></span>
<span data-ttu-id="823f1-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="823f1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="823f1-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="823f1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="823f1-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="823f1-143">-DefaultProfile</span></span>
<span data-ttu-id="823f1-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="823f1-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="823f1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="823f1-145">CommonParameters</span></span>
<span data-ttu-id="823f1-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="823f1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="823f1-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="823f1-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="823f1-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="823f1-148">INPUTS</span></span>

### <span data-ttu-id="823f1-149">String []</span><span class="sxs-lookup"><span data-stu-id="823f1-149">String[]</span></span>
<span data-ttu-id="823f1-150">' RESOURCEID ' parametresi ardışık düzenin ' String [] ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="823f1-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="823f1-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="823f1-151">OUTPUTS</span></span>

### <span data-ttu-id="823f1-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="823f1-152">System.Boolean</span></span>

## <span data-ttu-id="823f1-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="823f1-153">NOTES</span></span>

## <span data-ttu-id="823f1-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="823f1-154">RELATED LINKS</span></span>

[<span data-ttu-id="823f1-155">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="823f1-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="823f1-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="823f1-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="823f1-157">Yeni-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="823f1-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="823f1-158">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="823f1-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="823f1-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="823f1-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


