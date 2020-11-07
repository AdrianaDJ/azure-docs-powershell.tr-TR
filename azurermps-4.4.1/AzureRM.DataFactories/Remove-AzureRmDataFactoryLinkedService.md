---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: d3ea4c3f221a3d05c9d43e780cde359ff36843f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762880"
---
# <span data-ttu-id="81c59-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="81c59-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="81c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81c59-102">SYNOPSIS</span></span>
<span data-ttu-id="81c59-103">Azure Veri Fabrikası 'nden bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81c59-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81c59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81c59-104">SYNTAX</span></span>

### <span data-ttu-id="81c59-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="81c59-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81c59-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="81c59-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c59-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="81c59-107">DESCRIPTION</span></span>
<span data-ttu-id="81c59-108">**Remove-AzureRmDataFactoryLinkedService** cmdlet 'ı Azure Veri Fabrikası 'ndan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81c59-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="81c59-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81c59-109">EXAMPLES</span></span>

### <span data-ttu-id="81c59-110">Örnek 1: bağlantılı hizmeti kaldırma</span><span class="sxs-lookup"><span data-stu-id="81c59-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="81c59-111">Bu komut, WikiADF adlı Data Factory 'den LinkedServiceTest adlı bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81c59-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="81c59-112">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="81c59-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="81c59-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81c59-113">PARAMETERS</span></span>

### <span data-ttu-id="81c59-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="81c59-114">-DataFactory</span></span>
<span data-ttu-id="81c59-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c59-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="81c59-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81c59-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="81c59-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="81c59-117">-DataFactoryName</span></span>
<span data-ttu-id="81c59-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c59-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="81c59-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81c59-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="81c59-120">-Force</span><span class="sxs-lookup"><span data-stu-id="81c59-120">-Force</span></span>
<span data-ttu-id="81c59-121">Bu cmdlet 'in, sizden onay istemeden bağlantılı bir hizmeti kaldırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81c59-121">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="81c59-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="81c59-122">-Name</span></span>
<span data-ttu-id="81c59-123">Kaldırılacak bağlı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c59-123">Specifies the name of the linked service to remove.</span></span>

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

### <span data-ttu-id="81c59-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c59-124">-ResourceGroupName</span></span>
<span data-ttu-id="81c59-125">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c59-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="81c59-126">Bu cmdlet, bu parametrenin belirttiği gruptan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81c59-126">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="81c59-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="81c59-127">-Confirm</span></span>
<span data-ttu-id="81c59-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="81c59-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c59-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c59-129">-WhatIf</span></span>
<span data-ttu-id="81c59-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81c59-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c59-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="81c59-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c59-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c59-132">-DefaultProfile</span></span>
<span data-ttu-id="81c59-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81c59-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c59-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c59-134">CommonParameters</span></span>
<span data-ttu-id="81c59-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81c59-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c59-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c59-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c59-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81c59-137">INPUTS</span></span>

## <span data-ttu-id="81c59-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81c59-138">OUTPUTS</span></span>

### <span data-ttu-id="81c59-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81c59-139">System.Boolean</span></span>

## <span data-ttu-id="81c59-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81c59-140">NOTES</span></span>
* <span data-ttu-id="81c59-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="81c59-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="81c59-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81c59-142">RELATED LINKS</span></span>

[<span data-ttu-id="81c59-143">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="81c59-143">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="81c59-144">Yeni-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="81c59-144">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

