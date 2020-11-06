---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591005"
---
# <span data-ttu-id="3af14-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="3af14-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="3af14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3af14-102">SYNOPSIS</span></span>
<span data-ttu-id="3af14-103">Web servisinin anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3af14-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3af14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3af14-104">SYNTAX</span></span>

### <span data-ttu-id="3af14-105">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="3af14-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3af14-106">Getbyınstance</span><span class="sxs-lookup"><span data-stu-id="3af14-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3af14-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3af14-107">DESCRIPTION</span></span>
<span data-ttu-id="3af14-108">Azure Machine Learning Web servisinin çalışma zamanı API 'Lerinin erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3af14-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="3af14-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3af14-109">EXAMPLES</span></span>

### <span data-ttu-id="3af14-110">--------------------------Örnek 1-kaynak grubu ve adla belirtilen bir Web hizmeti için anahtarları alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="3af14-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="3af14-111">--------------------------Örnek 2-Web hizmeti örneğinin anahtarlarını alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="3af14-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="3af14-112">$mlService, Microsoft. Azure. Management. Machinöğrenim. WebServices. model. Webtürü türünde bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="3af14-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="3af14-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3af14-113">PARAMETERS</span></span>

### <span data-ttu-id="3af14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af14-114">-DefaultProfile</span></span>
<span data-ttu-id="3af14-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3af14-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af14-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="3af14-116">-MlWebService</span></span>
<span data-ttu-id="3af14-117">Erişim tuşlarının alındığı Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="3af14-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3af14-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="3af14-118">-Name</span></span>
<span data-ttu-id="3af14-119">Erişim tuşlarının alındığı Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="3af14-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af14-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af14-120">-ResourceGroupName</span></span>
<span data-ttu-id="3af14-121">Web hizmeti için kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3af14-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af14-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af14-122">CommonParameters</span></span>
<span data-ttu-id="3af14-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3af14-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af14-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af14-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af14-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3af14-125">INPUTS</span></span>

### <span data-ttu-id="3af14-126">Konumundaki</span><span class="sxs-lookup"><span data-stu-id="3af14-126">WebService</span></span>
<span data-ttu-id="3af14-127">' MlWebService ' parametresi ardışık düzenin ' WebService ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3af14-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="3af14-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3af14-128">OUTPUTS</span></span>

### <span data-ttu-id="3af14-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3af14-129">None</span></span>

## <span data-ttu-id="3af14-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3af14-130">NOTES</span></span>
<span data-ttu-id="3af14-131">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3af14-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3af14-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3af14-132">RELATED LINKS</span></span>

