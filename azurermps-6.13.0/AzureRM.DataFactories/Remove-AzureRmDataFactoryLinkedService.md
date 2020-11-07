---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7b4dd01a689e1ac7b87e1c83a1e19bbd0c8a86db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762980"
---
# <span data-ttu-id="72af2-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="72af2-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="72af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72af2-102">SYNOPSIS</span></span>
<span data-ttu-id="72af2-103">Azure Veri Fabrikası 'nden bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72af2-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72af2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72af2-104">SYNTAX</span></span>

### <span data-ttu-id="72af2-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="72af2-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72af2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="72af2-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72af2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72af2-107">DESCRIPTION</span></span>
<span data-ttu-id="72af2-108">**Remove-AzureRmDataFactoryLinkedService** cmdlet 'ı Azure Veri Fabrikası 'ndan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72af2-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="72af2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72af2-109">EXAMPLES</span></span>

### <span data-ttu-id="72af2-110">Örnek 1: bağlantılı hizmeti kaldırma</span><span class="sxs-lookup"><span data-stu-id="72af2-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="72af2-111">Bu komut, WikiADF adlı Data Factory 'den LinkedServiceTest adlı bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72af2-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="72af2-112">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="72af2-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="72af2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72af2-113">PARAMETERS</span></span>

### <span data-ttu-id="72af2-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="72af2-114">-DataFactory</span></span>
<span data-ttu-id="72af2-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72af2-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="72af2-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72af2-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72af2-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="72af2-117">-DataFactoryName</span></span>
<span data-ttu-id="72af2-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72af2-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="72af2-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72af2-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72af2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72af2-120">-DefaultProfile</span></span>
<span data-ttu-id="72af2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="72af2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72af2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="72af2-122">-Force</span></span>
<span data-ttu-id="72af2-123">Bu cmdlet 'in, sizden onay istemeden bağlantılı bir hizmeti kaldırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72af2-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="72af2-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="72af2-124">-Name</span></span>
<span data-ttu-id="72af2-125">Kaldırılacak bağlı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72af2-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72af2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72af2-126">-ResourceGroupName</span></span>
<span data-ttu-id="72af2-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72af2-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="72af2-128">Bu cmdlet, bu parametrenin belirttiği gruptan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72af2-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72af2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="72af2-129">-Confirm</span></span>
<span data-ttu-id="72af2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72af2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72af2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72af2-131">-WhatIf</span></span>
<span data-ttu-id="72af2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72af2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72af2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72af2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72af2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72af2-134">CommonParameters</span></span>
<span data-ttu-id="72af2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72af2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72af2-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72af2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72af2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72af2-137">INPUTS</span></span>

### <span data-ttu-id="72af2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="72af2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="72af2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="72af2-139">System.String</span></span>

## <span data-ttu-id="72af2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72af2-140">OUTPUTS</span></span>

### <span data-ttu-id="72af2-141">System. void</span><span class="sxs-lookup"><span data-stu-id="72af2-141">System.Void</span></span>

## <span data-ttu-id="72af2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72af2-142">NOTES</span></span>
* <span data-ttu-id="72af2-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="72af2-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="72af2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72af2-144">RELATED LINKS</span></span>

[<span data-ttu-id="72af2-145">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="72af2-145">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="72af2-146">Yeni-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="72af2-146">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


