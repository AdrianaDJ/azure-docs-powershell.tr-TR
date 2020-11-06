---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 5632de726797dd36af377f76b5919590c5826606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590205"
---
# <span data-ttu-id="5b236-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="5b236-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="5b236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b236-102">SYNOPSIS</span></span>
<span data-ttu-id="5b236-103">Bir veya daha fazla Web hizmeti için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="5b236-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b236-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b236-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b236-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b236-105">DESCRIPTION</span></span>
<span data-ttu-id="5b236-106">Web hizmeti tanım bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="5b236-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="5b236-107">Geçilen paralara bağlı olarak cmdlet, belirli bir Web hizmeti için bir tanım, geçerli abonelikteki belirli bir kaynak grubunun Web Hizmetleri için bir tanım koleksiyonu veya geçerli abonelikteki Web Hizmetleri için bir tanım koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="5b236-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="5b236-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b236-108">EXAMPLES</span></span>

### <span data-ttu-id="5b236-109">Örnek 1: belirli Web servisinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="5b236-109">Example 1: Get details of specific web service</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="5b236-110">Örnek 2: geçerli abonelikteki tüm Web hizmeti kaynaklarını alma</span><span class="sxs-lookup"><span data-stu-id="5b236-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzureRmMlWebService
```

### <span data-ttu-id="5b236-111">Örnek 3: geçerli abonelikteki ve verilen kaynak grubundaki tüm Web hizmetlerini edinin</span><span class="sxs-lookup"><span data-stu-id="5b236-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="5b236-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b236-112">PARAMETERS</span></span>

### <span data-ttu-id="5b236-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b236-113">-DefaultProfile</span></span>
<span data-ttu-id="5b236-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5b236-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b236-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b236-115">-Name</span></span>
<span data-ttu-id="5b236-116">Ayrıntılarının alındığı Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="5b236-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b236-117">-Bölge</span><span class="sxs-lookup"><span data-stu-id="5b236-117">-Region</span></span>
<span data-ttu-id="5b236-118">Regio adı</span><span class="sxs-lookup"><span data-stu-id="5b236-118">The name of regio</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b236-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b236-119">-ResourceGroupName</span></span>
<span data-ttu-id="5b236-120">Web servisinin ayrıntılarının alındığı kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="5b236-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b236-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b236-121">CommonParameters</span></span>
<span data-ttu-id="5b236-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b236-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b236-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b236-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b236-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b236-124">INPUTS</span></span>

### <span data-ttu-id="5b236-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5b236-125">None</span></span>

## <span data-ttu-id="5b236-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b236-126">OUTPUTS</span></span>

### <span data-ttu-id="5b236-127">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="5b236-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="5b236-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b236-128">NOTES</span></span>
<span data-ttu-id="5b236-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5b236-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5b236-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b236-130">RELATED LINKS</span></span>
