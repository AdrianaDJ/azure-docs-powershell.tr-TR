---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: f84973c29d83e8c7c01c3505d17166275a833460
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917051"
---
# <span data-ttu-id="51f21-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="51f21-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="51f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51f21-102">SYNOPSIS</span></span>
<span data-ttu-id="51f21-103">Veri Fabrikası 'ndan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51f21-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="51f21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51f21-104">SYNTAX</span></span>

### <span data-ttu-id="51f21-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51f21-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51f21-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="51f21-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51f21-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="51f21-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51f21-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="51f21-108">DESCRIPTION</span></span>
<span data-ttu-id="51f21-109">Remove-AzDataFactoryV2LinkedService cmdlet 'i Azure Veri Fabrikası 'ndan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51f21-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="51f21-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51f21-110">EXAMPLES</span></span>

### <span data-ttu-id="51f21-111">Örnek 1: bağlantılı hizmeti kaldırma</span><span class="sxs-lookup"><span data-stu-id="51f21-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="51f21-112">Bu komut, WikiADF adlı Data Factory 'den LinkedServiceTest adlı bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51f21-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="51f21-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="51f21-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="51f21-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51f21-114">PARAMETERS</span></span>

### <span data-ttu-id="51f21-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="51f21-115">-DataFactoryName</span></span>
<span data-ttu-id="51f21-116">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51f21-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="51f21-117">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51f21-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="51f21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f21-118">-DefaultProfile</span></span>
<span data-ttu-id="51f21-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51f21-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51f21-120">-Force</span><span class="sxs-lookup"><span data-stu-id="51f21-120">-Force</span></span>
<span data-ttu-id="51f21-121">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="51f21-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="51f21-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51f21-122">-InputObject</span></span>
<span data-ttu-id="51f21-123">Kaldırılacak LinkedService nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51f21-123">Specifies the LinkedService object to remove.</span></span>

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

### <span data-ttu-id="51f21-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="51f21-124">-Name</span></span>
<span data-ttu-id="51f21-125">Kaldırılacak bağlı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51f21-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="51f21-126">Bağlantılı hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="51f21-126">Name of the linked service.</span></span>

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

### <span data-ttu-id="51f21-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51f21-127">-ResourceGroupName</span></span>
<span data-ttu-id="51f21-128">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51f21-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="51f21-129">Bu cmdlet, bu parametrenin belirttiği gruptan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51f21-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="51f21-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="51f21-130">-ResourceId</span></span>
<span data-ttu-id="51f21-131">Kaldırılacak bağlı hizmetin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="51f21-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="51f21-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="51f21-132">-Confirm</span></span>
<span data-ttu-id="51f21-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51f21-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51f21-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f21-134">-WhatIf</span></span>
<span data-ttu-id="51f21-135">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="51f21-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="51f21-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f21-136">CommonParameters</span></span>
<span data-ttu-id="51f21-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51f21-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f21-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f21-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f21-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51f21-139">INPUTS</span></span>

### <span data-ttu-id="51f21-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="51f21-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="51f21-141">System. String</span><span class="sxs-lookup"><span data-stu-id="51f21-141">System.String</span></span>

## <span data-ttu-id="51f21-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51f21-142">OUTPUTS</span></span>

### <span data-ttu-id="51f21-143">System. void</span><span class="sxs-lookup"><span data-stu-id="51f21-143">System.Void</span></span>

## <span data-ttu-id="51f21-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51f21-144">NOTES</span></span>
<span data-ttu-id="51f21-145">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="51f21-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="51f21-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51f21-146">RELATED LINKS</span></span>

[<span data-ttu-id="51f21-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="51f21-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="51f21-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="51f21-148">Set-AzDataFactoryV2LinkedService</span></span>]()

