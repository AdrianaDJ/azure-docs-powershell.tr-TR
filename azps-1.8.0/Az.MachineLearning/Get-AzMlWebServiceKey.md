---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: a7e784d312ea834e30dac2243aefd880dca09dd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915884"
---
# <span data-ttu-id="904d0-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="904d0-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="904d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="904d0-102">SYNOPSIS</span></span>
<span data-ttu-id="904d0-103">Web servisinin anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="904d0-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="904d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="904d0-104">SYNTAX</span></span>

### <span data-ttu-id="904d0-105">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="904d0-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="904d0-106">Getbyınstance</span><span class="sxs-lookup"><span data-stu-id="904d0-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="904d0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="904d0-107">DESCRIPTION</span></span>
<span data-ttu-id="904d0-108">Azure Machine Learning Web servisinin çalışma zamanı API 'Lerinin erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="904d0-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="904d0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="904d0-109">EXAMPLES</span></span>

### <span data-ttu-id="904d0-110">Örnek 1-kaynak grubu ve adla belirtilen bir Web hizmeti için anahtarları alın</span><span class="sxs-lookup"><span data-stu-id="904d0-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="904d0-111">Örnek 2-Web hizmeti örneğinin anahtarlarını alın</span><span class="sxs-lookup"><span data-stu-id="904d0-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="904d0-112">$mlService, Microsoft. Azure. Management. Machinöğrenim. WebServices. model. Webtürü türünde bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="904d0-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="904d0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="904d0-113">PARAMETERS</span></span>

### <span data-ttu-id="904d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="904d0-114">-DefaultProfile</span></span>
<span data-ttu-id="904d0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="904d0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="904d0-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="904d0-116">-MlWebService</span></span>
<span data-ttu-id="904d0-117">Erişim tuşlarının alındığı Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="904d0-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="904d0-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="904d0-118">-Name</span></span>
<span data-ttu-id="904d0-119">Erişim tuşlarının alındığı Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="904d0-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="904d0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="904d0-120">-ResourceGroupName</span></span>
<span data-ttu-id="904d0-121">Web hizmeti için kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="904d0-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="904d0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="904d0-122">CommonParameters</span></span>
<span data-ttu-id="904d0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="904d0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="904d0-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="904d0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="904d0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="904d0-125">INPUTS</span></span>

### <span data-ttu-id="904d0-126">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="904d0-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="904d0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="904d0-127">OUTPUTS</span></span>

### <span data-ttu-id="904d0-128">Microsoft. Azure. Management. Machinöğrenim. WebServices. modeller. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="904d0-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="904d0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="904d0-129">NOTES</span></span>
<span data-ttu-id="904d0-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="904d0-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="904d0-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="904d0-131">RELATED LINKS</span></span>
