---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 0136927eea72911e706c3e0062dbc444cf1f9b25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761131"
---
# <span data-ttu-id="93095-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="93095-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="93095-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93095-102">SYNOPSIS</span></span>
<span data-ttu-id="93095-103">Azure Veri Fabrikası 'nden hub 'ı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93095-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="93095-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93095-104">SYNTAX</span></span>

### <span data-ttu-id="93095-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93095-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93095-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="93095-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93095-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="93095-107">DESCRIPTION</span></span>
<span data-ttu-id="93095-108">**Remove-AzDataFactoryHub** cmdlet 'i, belirtilen Azure Kaynak grubundaki ve belirtilen veri fabrikası 'Nde Azure Veri Fabrikası 'ndan hub 'ı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93095-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="93095-109">Bir hub 'ı kaldırırsanız, hub 'daki tüm bağlantılı hizmetler ve ardışık düzenler da kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="93095-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="93095-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93095-110">EXAMPLES</span></span>

### <span data-ttu-id="93095-111">Örnek 1: hub 'ı kaldırma</span><span class="sxs-lookup"><span data-stu-id="93095-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="93095-112">Bu komut, ADFResourceGroup adlı Azure Resource grubundan ContosoDataHub adlı hub 'ı ve ADFDataFactory adlı veri fabrikası 'nı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93095-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="93095-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93095-113">PARAMETERS</span></span>

### <span data-ttu-id="93095-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="93095-114">-DataFactory</span></span>
<span data-ttu-id="93095-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93095-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="93095-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93095-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="93095-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="93095-117">-DataFactoryName</span></span>
<span data-ttu-id="93095-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93095-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="93095-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93095-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="93095-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93095-120">-DefaultProfile</span></span>
<span data-ttu-id="93095-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="93095-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93095-122">-Force</span><span class="sxs-lookup"><span data-stu-id="93095-122">-Force</span></span>
<span data-ttu-id="93095-123">Bu cmdlet 'in bir hub 'ı onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93095-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="93095-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="93095-124">-Name</span></span>
<span data-ttu-id="93095-125">Kaldırılacak hub 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93095-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93095-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93095-126">-ResourceGroupName</span></span>
<span data-ttu-id="93095-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93095-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="93095-128">Bu cmdlet, bu parametrenin belirttiği gruptan bir hub kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93095-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="93095-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="93095-129">-Confirm</span></span>
<span data-ttu-id="93095-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93095-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93095-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93095-131">-WhatIf</span></span>
<span data-ttu-id="93095-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93095-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93095-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93095-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93095-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93095-134">CommonParameters</span></span>
<span data-ttu-id="93095-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93095-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93095-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93095-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93095-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93095-137">INPUTS</span></span>

### <span data-ttu-id="93095-138">System. String</span><span class="sxs-lookup"><span data-stu-id="93095-138">System.String</span></span>

### <span data-ttu-id="93095-139">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="93095-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="93095-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93095-140">OUTPUTS</span></span>

### <span data-ttu-id="93095-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93095-141">System.Boolean</span></span>

## <span data-ttu-id="93095-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93095-142">NOTES</span></span>
* <span data-ttu-id="93095-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="93095-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="93095-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93095-144">RELATED LINKS</span></span>

[<span data-ttu-id="93095-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="93095-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="93095-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="93095-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


