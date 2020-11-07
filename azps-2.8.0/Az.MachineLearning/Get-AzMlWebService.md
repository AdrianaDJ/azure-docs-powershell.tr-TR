---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: 73e20db774e6df70086eef6dc61a2ba9ecfb8689
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751454"
---
# <span data-ttu-id="acdf1-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="acdf1-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="acdf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acdf1-102">SYNOPSIS</span></span>
<span data-ttu-id="acdf1-103">Bir veya daha fazla Web hizmeti için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="acdf1-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="acdf1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acdf1-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acdf1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="acdf1-105">DESCRIPTION</span></span>
<span data-ttu-id="acdf1-106">Web hizmeti tanım bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="acdf1-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="acdf1-107">Geçirilen parametrelere bağlı olarak, cmdlet belirli bir Web hizmetinin tanımını, geçerli abonelikteki belirli bir kaynak grubunun Web Hizmetleri için bir tanım koleksiyonu veya geçerli abonelikteki Web Hizmetleri için bir tanımlar koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="acdf1-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="acdf1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acdf1-108">EXAMPLES</span></span>

### <span data-ttu-id="acdf1-109">Örnek 1: belirli Web servisinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="acdf1-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="acdf1-110">Örnek 2: geçerli abonelikteki tüm Web hizmeti kaynaklarını alma</span><span class="sxs-lookup"><span data-stu-id="acdf1-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="acdf1-111">Örnek 3: geçerli abonelikteki ve verilen kaynak grubundaki tüm Web hizmetlerini edinin</span><span class="sxs-lookup"><span data-stu-id="acdf1-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="acdf1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acdf1-112">PARAMETERS</span></span>

### <span data-ttu-id="acdf1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acdf1-113">-DefaultProfile</span></span>
<span data-ttu-id="acdf1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="acdf1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acdf1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="acdf1-115">-Name</span></span>
<span data-ttu-id="acdf1-116">Ayrıntılarının alındığı Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="acdf1-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="acdf1-117">-Bölge</span><span class="sxs-lookup"><span data-stu-id="acdf1-117">-Region</span></span>
<span data-ttu-id="acdf1-118">Bölge adı</span><span class="sxs-lookup"><span data-stu-id="acdf1-118">The name of region</span></span>

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

### <span data-ttu-id="acdf1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acdf1-119">-ResourceGroupName</span></span>
<span data-ttu-id="acdf1-120">Web servisinin ayrıntılarının alındığı kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="acdf1-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="acdf1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdf1-121">CommonParameters</span></span>
<span data-ttu-id="acdf1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acdf1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdf1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acdf1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdf1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acdf1-124">INPUTS</span></span>

### <span data-ttu-id="acdf1-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="acdf1-125">None</span></span>

## <span data-ttu-id="acdf1-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acdf1-126">OUTPUTS</span></span>

### <span data-ttu-id="acdf1-127">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="acdf1-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="acdf1-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acdf1-128">NOTES</span></span>
<span data-ttu-id="acdf1-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="acdf1-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="acdf1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acdf1-130">RELATED LINKS</span></span>