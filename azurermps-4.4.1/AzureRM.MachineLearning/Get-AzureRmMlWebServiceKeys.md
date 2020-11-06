---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594651"
---
# <span data-ttu-id="eeaf3-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="eeaf3-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="eeaf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeaf3-102">SYNOPSIS</span></span>
<span data-ttu-id="eeaf3-103">Web servisinin anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeaf3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eeaf3-104">SYNTAX</span></span>

### <span data-ttu-id="eeaf3-105">Bir Azure ML Web servisinin erişim tuşlarından birinin adı ve kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeaf3-106">Verilen Web hizmeti örneğinin erişim kesy edinin.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eeaf3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eeaf3-107">DESCRIPTION</span></span>
<span data-ttu-id="eeaf3-108">Azure Machine Learning Web servisinin çalışma zamanı API 'Lerinin erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="eeaf3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eeaf3-109">EXAMPLES</span></span>

### <span data-ttu-id="eeaf3-110">--------------------------Örnek 1-kaynak grubu ve adla belirtilen bir Web hizmeti için anahtarları alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="eeaf3-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="eeaf3-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="eeaf3-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="eeaf3-112">--------------------------Örnek 2-Web hizmeti örneğinin anahtarlarını alın--------------------------</span><span class="sxs-lookup"><span data-stu-id="eeaf3-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="eeaf3-113">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="eeaf3-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="eeaf3-114">$mlService, Microsoft. Azure. Management. Machinöğrenim. WebServices. model. Webtürü türünde bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="eeaf3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eeaf3-115">PARAMETERS</span></span>

### <span data-ttu-id="eeaf3-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="eeaf3-116">-MlWebService</span></span>
<span data-ttu-id="eeaf3-117">Erişim tuşlarının alındığı Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeaf3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="eeaf3-118">-Name</span></span>
<span data-ttu-id="eeaf3-119">Erişim tuşlarının alındığı Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeaf3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeaf3-120">-ResourceGroupName</span></span>
<span data-ttu-id="eeaf3-121">Web hizmeti için kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeaf3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeaf3-122">-DefaultProfile</span></span>
<span data-ttu-id="eeaf3-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeaf3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeaf3-124">CommonParameters</span></span>
<span data-ttu-id="eeaf3-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eeaf3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeaf3-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeaf3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeaf3-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eeaf3-127">INPUTS</span></span>

### <span data-ttu-id="eeaf3-128">Konumundaki</span><span class="sxs-lookup"><span data-stu-id="eeaf3-128">WebService</span></span>
<span data-ttu-id="eeaf3-129">' MlWebService ' parametresi ardışık düzenin ' WebService ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="eeaf3-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="eeaf3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eeaf3-130">OUTPUTS</span></span>

### <span data-ttu-id="eeaf3-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eeaf3-131">None</span></span>

## <span data-ttu-id="eeaf3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eeaf3-132">NOTES</span></span>
<span data-ttu-id="eeaf3-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="eeaf3-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="eeaf3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eeaf3-134">RELATED LINKS</span></span>

