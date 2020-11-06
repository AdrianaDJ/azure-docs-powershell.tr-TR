---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: bba4df58ed4046eeba562e3438119e1d5df40649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591770"
---
# <span data-ttu-id="abf68-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="abf68-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="abf68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf68-102">SYNOPSIS</span></span>
<span data-ttu-id="abf68-103">Veri Fabrikası 'ndan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abf68-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abf68-104">SYNTAX</span></span>

### <span data-ttu-id="abf68-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="abf68-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abf68-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="abf68-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abf68-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="abf68-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abf68-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="abf68-108">DESCRIPTION</span></span>
<span data-ttu-id="abf68-109">Remove-AzureRmDataFactoryV2LinkedService cmdlet 'i Azure Veri Fabrikası 'ndan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abf68-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="abf68-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abf68-110">EXAMPLES</span></span>

### <span data-ttu-id="abf68-111">Örnek 1: bağlantılı hizmeti kaldırma</span><span class="sxs-lookup"><span data-stu-id="abf68-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="abf68-112">Bu komut, WikiADF adlı Data Factory 'den LinkedServiceTest adlı bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abf68-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="abf68-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="abf68-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="abf68-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abf68-114">PARAMETERS</span></span>

### <span data-ttu-id="abf68-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="abf68-115">-Confirm</span></span>
<span data-ttu-id="abf68-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="abf68-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf68-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="abf68-117">-DataFactoryName</span></span>
<span data-ttu-id="abf68-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf68-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="abf68-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abf68-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="abf68-120">-Force</span><span class="sxs-lookup"><span data-stu-id="abf68-120">-Force</span></span>
<span data-ttu-id="abf68-121">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="abf68-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="abf68-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abf68-122">-InputObject</span></span>
<span data-ttu-id="abf68-123">Kaldırılacak LinkedService nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf68-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abf68-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="abf68-124">-Name</span></span>
<span data-ttu-id="abf68-125">Kaldırılacak bağlı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf68-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="abf68-126">Bağlantılı hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="abf68-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf68-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf68-127">-ResourceGroupName</span></span>
<span data-ttu-id="abf68-128">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf68-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="abf68-129">Bu cmdlet, bu parametrenin belirttiği gruptan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abf68-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="abf68-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="abf68-130">-ResourceId</span></span>
<span data-ttu-id="abf68-131">Kaldırılacak bağlı hizmetin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="abf68-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf68-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf68-132">-WhatIf</span></span>
<span data-ttu-id="abf68-133">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="abf68-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf68-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf68-134">-DefaultProfile</span></span>
<span data-ttu-id="abf68-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abf68-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf68-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf68-136">CommonParameters</span></span>
<span data-ttu-id="abf68-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abf68-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf68-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf68-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf68-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abf68-139">INPUTS</span></span>

### <span data-ttu-id="abf68-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="abf68-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="abf68-141">System. String</span><span class="sxs-lookup"><span data-stu-id="abf68-141">System.String</span></span>

## <span data-ttu-id="abf68-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abf68-142">OUTPUTS</span></span>

### <span data-ttu-id="abf68-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="abf68-143">System.Object</span></span>

## <span data-ttu-id="abf68-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abf68-144">NOTES</span></span>
<span data-ttu-id="abf68-145">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="abf68-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="abf68-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abf68-146">RELATED LINKS</span></span>

[<span data-ttu-id="abf68-147">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="abf68-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="abf68-148">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="abf68-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

