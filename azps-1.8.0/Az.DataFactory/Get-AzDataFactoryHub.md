---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 84608cbe83d54d562877aa2ada4527fbc636996f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761163"
---
# <span data-ttu-id="d9258-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d9258-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="d9258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9258-102">SYNOPSIS</span></span>
<span data-ttu-id="d9258-103">Azure Veri Fabrikası 'nde Hub 'lar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d9258-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="d9258-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9258-104">SYNTAX</span></span>

### <span data-ttu-id="d9258-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d9258-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9258-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d9258-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9258-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9258-107">DESCRIPTION</span></span>
<span data-ttu-id="d9258-108">**Get-AzDataFactoryHub** cmdlet 'ı Azure Veri Fabrikası 'nde Hub 'lar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d9258-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="d9258-109">Bir hub adı belirtirseniz, bu cmdlet bu hub hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d9258-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="d9258-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm Hub 'lar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d9258-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="d9258-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9258-111">EXAMPLES</span></span>

### <span data-ttu-id="d9258-112">Örnek 1: tüm veri hub 'ları</span><span class="sxs-lookup"><span data-stu-id="d9258-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="d9258-113">Bu komut, ADFResourceGroup adlı Azure Resource grubundaki tüm veri hub 'ları ve ADFDataFactory adlı veri fabrikası alır.</span><span class="sxs-lookup"><span data-stu-id="d9258-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="d9258-114">Örnek 2: belirli bir veri hub 'ı edinin</span><span class="sxs-lookup"><span data-stu-id="d9258-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="d9258-115">Bu komut, ADFResourceGroup adlı Azure Resource grubunda MyDataHub adlı hub ve ADFDataFactory adlı veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d9258-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="d9258-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9258-116">PARAMETERS</span></span>

### <span data-ttu-id="d9258-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d9258-117">-DataFactory</span></span>
<span data-ttu-id="d9258-118">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9258-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d9258-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içindeki Hublar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d9258-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9258-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d9258-120">-DataFactoryName</span></span>
<span data-ttu-id="d9258-121">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9258-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d9258-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içindeki Hublar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d9258-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9258-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9258-123">-DefaultProfile</span></span>
<span data-ttu-id="d9258-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d9258-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9258-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9258-125">-Name</span></span>
<span data-ttu-id="d9258-126">Bilgi alınacak hub 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9258-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="d9258-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9258-127">-ResourceGroupName</span></span>
<span data-ttu-id="d9258-128">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9258-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d9258-129">Bu cmdlet, bu parametrenin belirttiği gruba ait olan Hublar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d9258-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9258-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9258-130">CommonParameters</span></span>
<span data-ttu-id="d9258-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9258-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9258-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9258-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9258-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9258-133">INPUTS</span></span>

### <span data-ttu-id="d9258-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d9258-134">System.String</span></span>

### <span data-ttu-id="d9258-135">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="d9258-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d9258-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9258-136">OUTPUTS</span></span>

### <span data-ttu-id="d9258-137">Microsoft. Azure. Commands. DataFactory. modeller. PSHub</span><span class="sxs-lookup"><span data-stu-id="d9258-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="d9258-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9258-138">NOTES</span></span>
* <span data-ttu-id="d9258-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="d9258-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d9258-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9258-140">RELATED LINKS</span></span>

[<span data-ttu-id="d9258-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d9258-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="d9258-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d9258-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


