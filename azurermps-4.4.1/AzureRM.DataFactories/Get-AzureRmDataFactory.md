---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 5a7faf2e3eebcb00650bce367747e1945f7524da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588001"
---
# <span data-ttu-id="96aa6-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="96aa6-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="96aa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="96aa6-103">Veri Fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="96aa6-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96aa6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96aa6-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96aa6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="96aa6-106">**Get-AzureRmDataFactory** cmdlet 'i, bir Azure Kaynak grubundaki veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="96aa6-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="96aa6-107">Veri Fabrikası adı belirtirseniz, bu cmdlet bu veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="96aa6-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="96aa6-108">Bir ad belirtmezseniz, bu cmdlet bir Azure Kaynak grubundaki tüm veri fabrikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="96aa6-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="96aa6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96aa6-109">EXAMPLES</span></span>

### <span data-ttu-id="96aa6-110">Örnek 1: tüm veri fabrikaları</span><span class="sxs-lookup"><span data-stu-id="96aa6-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
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

<span data-ttu-id="96aa6-111">Bu komut, Azure aboneliğindeki tüm veri fabrikaları hakkında bilgi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="96aa6-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="96aa6-112">Örnek 2: belirli bir veri fabrikası edinin</span><span class="sxs-lookup"><span data-stu-id="96aa6-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="96aa6-113">Bu komut, ADF adlı kaynak grubu için aboneliğindeki WikiADF adlı veri fabrikası hakkında bilgi görüntüler ve $DataFactory değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="96aa6-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="96aa6-114">$DataFactory 'da depolanan veri fabrikasını kullanmak için sonraki cmdlet lerde *DataFactory* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="96aa6-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="96aa6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96aa6-115">PARAMETERS</span></span>

### <span data-ttu-id="96aa6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="96aa6-116">-Name</span></span>
<span data-ttu-id="96aa6-117">Bilgi alınacak veri fabrikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96aa6-117">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="96aa6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96aa6-118">-ResourceGroupName</span></span>
<span data-ttu-id="96aa6-119">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="96aa6-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="96aa6-120">Bu cmdlet, bu parametrenin belirttiği gruba ait veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="96aa6-120">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="96aa6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96aa6-121">-DefaultProfile</span></span>
<span data-ttu-id="96aa6-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96aa6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96aa6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96aa6-123">CommonParameters</span></span>
<span data-ttu-id="96aa6-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96aa6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96aa6-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96aa6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96aa6-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96aa6-126">INPUTS</span></span>

## <span data-ttu-id="96aa6-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96aa6-127">OUTPUTS</span></span>

### <span data-ttu-id="96aa6-128">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDAtafabrikası, Microsoft. Windowsazve. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="96aa6-128">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="96aa6-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96aa6-129">NOTES</span></span>
* <span data-ttu-id="96aa6-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="96aa6-130">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="96aa6-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96aa6-131">RELATED LINKS</span></span>

[<span data-ttu-id="96aa6-132">Yeni-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="96aa6-132">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="96aa6-133">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="96aa6-133">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


