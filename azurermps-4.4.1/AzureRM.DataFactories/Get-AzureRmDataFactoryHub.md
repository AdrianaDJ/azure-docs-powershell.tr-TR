---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: a96d8d3d9025e473b5c08d84201fde2a10d8be34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594761"
---
# <span data-ttu-id="732b0-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="732b0-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="732b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="732b0-102">SYNOPSIS</span></span>
<span data-ttu-id="732b0-103">Azure Veri Fabrikası 'nde Hub 'lar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="732b0-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="732b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="732b0-104">SYNTAX</span></span>

### <span data-ttu-id="732b0-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="732b0-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="732b0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="732b0-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="732b0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="732b0-107">DESCRIPTION</span></span>
<span data-ttu-id="732b0-108">**Get-AzureRmDataFactoryHub** cmdlet 'ı Azure Veri Fabrikası 'ndaki Hublar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="732b0-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="732b0-109">Bir hub adı belirtirseniz, bu cmdlet bu hub hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="732b0-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="732b0-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm Hub 'lar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="732b0-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="732b0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="732b0-111">EXAMPLES</span></span>

### <span data-ttu-id="732b0-112">Örnek 1: tüm veri hub 'ları</span><span class="sxs-lookup"><span data-stu-id="732b0-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="732b0-113">Bu komut, ADFResourceGroup adlı Azure Resource grubundaki tüm veri hub 'ları ve ADFDataFactory adlı veri fabrikası alır.</span><span class="sxs-lookup"><span data-stu-id="732b0-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="732b0-114">Örnek 2: belirli bir veri hub 'ı edinin</span><span class="sxs-lookup"><span data-stu-id="732b0-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="732b0-115">Bu komut, ADFResourceGroup adlı Azure Resource grubunda MyDataHub adlı hub ve ADFDataFactory adlı veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="732b0-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="732b0-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="732b0-116">PARAMETERS</span></span>

### <span data-ttu-id="732b0-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="732b0-117">-DataFactory</span></span>
<span data-ttu-id="732b0-118">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="732b0-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="732b0-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içindeki Hublar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="732b0-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="732b0-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="732b0-120">-DataFactoryName</span></span>
<span data-ttu-id="732b0-121">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="732b0-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="732b0-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içindeki Hublar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="732b0-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="732b0-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="732b0-123">-Name</span></span>
<span data-ttu-id="732b0-124">Bilgi alınacak hub 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="732b0-124">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="732b0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="732b0-125">-ResourceGroupName</span></span>
<span data-ttu-id="732b0-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="732b0-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="732b0-127">Bu cmdlet, bu parametrenin belirttiği gruba ait olan Hublar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="732b0-127">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="732b0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732b0-128">-DefaultProfile</span></span>
<span data-ttu-id="732b0-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="732b0-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="732b0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732b0-130">CommonParameters</span></span>
<span data-ttu-id="732b0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="732b0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732b0-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="732b0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732b0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="732b0-133">INPUTS</span></span>

## <span data-ttu-id="732b0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="732b0-134">OUTPUTS</span></span>

### <span data-ttu-id="732b0-135">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. DataFactory. modeller. PSHub]</span><span class="sxs-lookup"><span data-stu-id="732b0-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.DataFactories.Models.PSHub]</span></span>

### <span data-ttu-id="732b0-136">Microsoft. Azure. Commands. DataFactory. modeller. PSHub</span><span class="sxs-lookup"><span data-stu-id="732b0-136">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="732b0-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="732b0-137">NOTES</span></span>
* <span data-ttu-id="732b0-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="732b0-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="732b0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="732b0-139">RELATED LINKS</span></span>

[<span data-ttu-id="732b0-140">Yeni-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="732b0-140">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="732b0-141">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="732b0-141">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


