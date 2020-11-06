---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
ms.openlocfilehash: 6788f2dea9cf46b888f729ab97640201f740e80d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591785"
---
# <span data-ttu-id="61d34-101">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="61d34-101">Remove-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="61d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61d34-102">SYNOPSIS</span></span>
<span data-ttu-id="61d34-103">Azure Veri Fabrikası 'nden hub 'ı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61d34-103">Removes a hub from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61d34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61d34-104">SYNTAX</span></span>

### <span data-ttu-id="61d34-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61d34-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61d34-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="61d34-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61d34-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="61d34-107">DESCRIPTION</span></span>
<span data-ttu-id="61d34-108">**Remove-AzureRmDataFactoryHub** cmdlet 'ı belirtilen Azure Kaynak grubundaki ve belirtilen veri fabrikasında Azure Veri Fabrikası 'ndan bir hub kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61d34-108">The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="61d34-109">Bir hub 'ı kaldırırsanız, hub 'daki tüm bağlantılı hizmetler ve ardışık düzenler da kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="61d34-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="61d34-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61d34-110">EXAMPLES</span></span>

### <span data-ttu-id="61d34-111">Örnek 1: hub 'ı kaldırma</span><span class="sxs-lookup"><span data-stu-id="61d34-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="61d34-112">Bu komut, ADFResourceGroup adlı Azure Resource grubundan ContosoDataHub adlı hub 'ı ve ADFDataFactory adlı veri fabrikası 'nı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61d34-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="61d34-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61d34-113">PARAMETERS</span></span>

### <span data-ttu-id="61d34-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="61d34-114">-DataFactory</span></span>
<span data-ttu-id="61d34-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61d34-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="61d34-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61d34-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="61d34-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="61d34-117">-DataFactoryName</span></span>
<span data-ttu-id="61d34-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61d34-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="61d34-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61d34-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="61d34-120">-Force</span><span class="sxs-lookup"><span data-stu-id="61d34-120">-Force</span></span>
<span data-ttu-id="61d34-121">Bu cmdlet 'in bir hub 'ı onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61d34-121">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="61d34-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="61d34-122">-Name</span></span>
<span data-ttu-id="61d34-123">Kaldırılacak hub 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61d34-123">Specifies the name of the hub to remove.</span></span>

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

### <span data-ttu-id="61d34-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d34-124">-ResourceGroupName</span></span>
<span data-ttu-id="61d34-125">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61d34-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="61d34-126">Bu cmdlet, bu parametrenin belirttiği gruptan bir hub kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61d34-126">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="61d34-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="61d34-127">-Confirm</span></span>
<span data-ttu-id="61d34-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61d34-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d34-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d34-129">-WhatIf</span></span>
<span data-ttu-id="61d34-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61d34-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d34-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61d34-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d34-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d34-132">-DefaultProfile</span></span>
<span data-ttu-id="61d34-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61d34-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61d34-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d34-134">CommonParameters</span></span>
<span data-ttu-id="61d34-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61d34-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d34-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d34-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d34-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61d34-137">INPUTS</span></span>

## <span data-ttu-id="61d34-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61d34-138">OUTPUTS</span></span>

### <span data-ttu-id="61d34-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61d34-139">System.Boolean</span></span>

## <span data-ttu-id="61d34-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61d34-140">NOTES</span></span>
* <span data-ttu-id="61d34-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="61d34-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="61d34-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61d34-142">RELATED LINKS</span></span>

[<span data-ttu-id="61d34-143">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="61d34-143">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="61d34-144">Yeni-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="61d34-144">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)


