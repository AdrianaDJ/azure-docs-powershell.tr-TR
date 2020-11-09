---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321081"
---
# <span data-ttu-id="5699a-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="5699a-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="5699a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5699a-102">SYNOPSIS</span></span>
<span data-ttu-id="5699a-103">Veri Fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5699a-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="5699a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5699a-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5699a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5699a-105">DESCRIPTION</span></span>
<span data-ttu-id="5699a-106">**Get-AzDataFactory** cmdlet 'ı bir Azure Kaynak grubundaki veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5699a-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="5699a-107">Veri Fabrikası adı belirtirseniz, bu cmdlet bu veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5699a-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="5699a-108">Bir ad belirtmezseniz, bu cmdlet bir Azure Kaynak grubundaki tüm veri fabrikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5699a-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="5699a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5699a-109">EXAMPLES</span></span>

### <span data-ttu-id="5699a-110">Örnek 1: tüm veri fabrikaları</span><span class="sxs-lookup"><span data-stu-id="5699a-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="5699a-111">Bu komut, Azure aboneliğindeki tüm veri fabrikaları hakkında bilgi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="5699a-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="5699a-112">Örnek 2: belirli bir veri fabrikası edinin</span><span class="sxs-lookup"><span data-stu-id="5699a-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="5699a-113">Bu komut, ADF adlı kaynak grubu için aboneliğindeki WikiADF adlı veri fabrikası hakkında bilgi görüntüler ve $DataFactory değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5699a-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="5699a-114">$DataFactory 'da depolanan veri fabrikasını kullanmak için sonraki cmdlet lerde *DataFactory* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5699a-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="5699a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5699a-115">PARAMETERS</span></span>

### <span data-ttu-id="5699a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5699a-116">-DefaultProfile</span></span>
<span data-ttu-id="5699a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5699a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5699a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="5699a-118">-Name</span></span>
<span data-ttu-id="5699a-119">Bilgi alınacak veri fabrikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5699a-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5699a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5699a-120">-ResourceGroupName</span></span>
<span data-ttu-id="5699a-121">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5699a-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5699a-122">Bu cmdlet, bu parametrenin belirttiği gruba ait veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5699a-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5699a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5699a-123">CommonParameters</span></span>
<span data-ttu-id="5699a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5699a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5699a-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5699a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5699a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5699a-126">INPUTS</span></span>

### <span data-ttu-id="5699a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5699a-127">System.String</span></span>

## <span data-ttu-id="5699a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5699a-128">OUTPUTS</span></span>

### <span data-ttu-id="5699a-129">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="5699a-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="5699a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5699a-130">NOTES</span></span>
* <span data-ttu-id="5699a-131">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="5699a-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5699a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5699a-132">RELATED LINKS</span></span>

[<span data-ttu-id="5699a-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="5699a-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="5699a-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="5699a-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


