---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: c121834f618dacdb1c2116852b7537f88d323bd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761140"
---
# <span data-ttu-id="16539-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="16539-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="16539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16539-102">SYNOPSIS</span></span>
<span data-ttu-id="16539-103">Azure Veri Fabrikası için bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16539-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="16539-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16539-104">SYNTAX</span></span>

### <span data-ttu-id="16539-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16539-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16539-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="16539-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16539-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="16539-107">DESCRIPTION</span></span>
<span data-ttu-id="16539-108">**New-AzDataFactoryHub** cmdlet 'ı belirtilen Azure Resource grubunda ve belirtilen veri fabrikası içinde belirtilen dosya tanımıyla Azure Veri Fabrikası için bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16539-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="16539-109">Hub 'ı oluşturduktan sonra, bir grupta bağlantılı hizmetleri depolamak ve yönetmek için kullanabilirsiniz ve merkeze ardışık düzen ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16539-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="16539-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16539-110">EXAMPLES</span></span>

### <span data-ttu-id="16539-111">Örnek 1: hub oluşturma</span><span class="sxs-lookup"><span data-stu-id="16539-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="16539-112">Bu komut, ADFResourceGroup kaynak grubunda ContosoDataHub adlı bir hub ve ADFDataFactory adlı veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16539-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="16539-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16539-113">PARAMETERS</span></span>

### <span data-ttu-id="16539-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="16539-114">-DataFactory</span></span>
<span data-ttu-id="16539-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16539-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="16539-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16539-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="16539-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="16539-117">-DataFactoryName</span></span>
<span data-ttu-id="16539-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16539-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="16539-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16539-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="16539-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16539-120">-DefaultProfile</span></span>
<span data-ttu-id="16539-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16539-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16539-122">-Dosya</span><span class="sxs-lookup"><span data-stu-id="16539-122">-File</span></span>
<span data-ttu-id="16539-123">Hub 'ın açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="16539-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16539-124">-Force</span><span class="sxs-lookup"><span data-stu-id="16539-124">-Force</span></span>
<span data-ttu-id="16539-125">Bu cmdlet 'in mevcut bir hub 'ın yerini onaylamanızı istemeden değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16539-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="16539-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="16539-126">-Name</span></span>
<span data-ttu-id="16539-127">Oluşturulacak hub 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16539-127">Specifies the name of the hub to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16539-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16539-128">-ResourceGroupName</span></span>
<span data-ttu-id="16539-129">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16539-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="16539-130">Bu cmdlet, bu parametrenin belirttiği gruba ait bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="16539-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="16539-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="16539-131">-Confirm</span></span>
<span data-ttu-id="16539-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16539-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16539-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16539-133">-WhatIf</span></span>
<span data-ttu-id="16539-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16539-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16539-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16539-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16539-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16539-136">CommonParameters</span></span>
<span data-ttu-id="16539-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16539-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16539-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16539-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16539-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16539-139">INPUTS</span></span>

### <span data-ttu-id="16539-140">System. String</span><span class="sxs-lookup"><span data-stu-id="16539-140">System.String</span></span>

### <span data-ttu-id="16539-141">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="16539-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="16539-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16539-142">OUTPUTS</span></span>

### <span data-ttu-id="16539-143">Microsoft. Azure. Commands. DataFactory. modeller. PSHub</span><span class="sxs-lookup"><span data-stu-id="16539-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="16539-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16539-144">NOTES</span></span>
* <span data-ttu-id="16539-145">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="16539-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="16539-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16539-146">RELATED LINKS</span></span>

[<span data-ttu-id="16539-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="16539-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="16539-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="16539-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


