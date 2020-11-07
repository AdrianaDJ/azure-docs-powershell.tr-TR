---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
ms.openlocfilehash: d92cb12f051095a7e5de47d9c12b2c2329841bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590745"
---
# <span data-ttu-id="b3ab2-101">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="b3ab2-101">New-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="b3ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ab2-103">Azure Veri Fabrikası için bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-103">Creates a hub for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3ab2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3ab2-104">SYNTAX</span></span>

### <span data-ttu-id="b3ab2-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3ab2-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3ab2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b3ab2-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3ab2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3ab2-107">DESCRIPTION</span></span>
<span data-ttu-id="b3ab2-108">**New-AzureRmDataFactoryHub** cmdlet 'ı belirtilen Azure Kaynak grubunda ve belirtilen veri fabrikası içinde belirtilen dosya tanımıyla Azure Veri Fabrikası için bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-108">The **New-AzureRmDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="b3ab2-109">Hub 'ı oluşturduktan sonra, bir grupta bağlantılı hizmetleri depolamak ve yönetmek için kullanabilirsiniz ve merkeze ardışık düzen ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="b3ab2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3ab2-110">EXAMPLES</span></span>

### <span data-ttu-id="b3ab2-111">Örnek 1: hub oluşturma</span><span class="sxs-lookup"><span data-stu-id="b3ab2-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="b3ab2-112">Bu komut, ADFResourceGroup kaynak grubunda ContosoDataHub adlı bir hub ve ADFDataFactory adlı veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="b3ab2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3ab2-113">PARAMETERS</span></span>

### <span data-ttu-id="b3ab2-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3ab2-114">-DataFactory</span></span>
<span data-ttu-id="b3ab2-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b3ab2-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3ab2-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b3ab2-117">-DataFactoryName</span></span>
<span data-ttu-id="b3ab2-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b3ab2-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3ab2-120">-Dosya</span><span class="sxs-lookup"><span data-stu-id="b3ab2-120">-File</span></span>
<span data-ttu-id="b3ab2-121">Hub 'ın açıklamasını içeren JavaScript nesne Gösterim (JSON) dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-121">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="b3ab2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b3ab2-122">-Force</span></span>
<span data-ttu-id="b3ab2-123">Bu cmdlet 'in mevcut bir hub 'ın yerini onaylamanızı istemeden değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-123">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b3ab2-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3ab2-124">-Name</span></span>
<span data-ttu-id="b3ab2-125">Oluşturulacak hub 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-125">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="b3ab2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ab2-126">-ResourceGroupName</span></span>
<span data-ttu-id="b3ab2-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b3ab2-128">Bu cmdlet, bu parametrenin belirttiği gruba ait bir hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-128">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3ab2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3ab2-129">-Confirm</span></span>
<span data-ttu-id="b3ab2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ab2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ab2-131">-WhatIf</span></span>
<span data-ttu-id="b3ab2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ab2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ab2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ab2-134">-DefaultProfile</span></span>
<span data-ttu-id="b3ab2-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3ab2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ab2-136">CommonParameters</span></span>
<span data-ttu-id="b3ab2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3ab2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ab2-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ab2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ab2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3ab2-139">INPUTS</span></span>

## <span data-ttu-id="b3ab2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3ab2-140">OUTPUTS</span></span>

### <span data-ttu-id="b3ab2-141">Microsoft. Azure. Commands. DataFactory. modeller. PSHub</span><span class="sxs-lookup"><span data-stu-id="b3ab2-141">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="b3ab2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3ab2-142">NOTES</span></span>
* <span data-ttu-id="b3ab2-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="b3ab2-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b3ab2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3ab2-144">RELATED LINKS</span></span>

[<span data-ttu-id="b3ab2-145">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="b3ab2-145">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="b3ab2-146">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="b3ab2-146">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)

