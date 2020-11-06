---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594655"
---
# <span data-ttu-id="c4d11-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="c4d11-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="c4d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4d11-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d11-103">Bir veya daha fazla Web hizmeti için Özet bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="c4d11-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4d11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4d11-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4d11-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4d11-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d11-106">Web hizmeti tanım bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="c4d11-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="c4d11-107">Geçilen paralara bağlı olarak cmdlet, belirli bir Web hizmeti için bir tanım, geçerli abonelikteki belirli bir kaynak grubunun Web Hizmetleri için bir tanım koleksiyonu veya geçerli abonelikteki Web Hizmetleri için bir tanım koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="c4d11-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="c4d11-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4d11-108">EXAMPLES</span></span>

### <span data-ttu-id="c4d11-109">--------------------------Örnek 1: belirli Web hizmetinin ayrıntılarını alma--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4d11-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="c4d11-110">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="c4d11-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="c4d11-111">--------------------------Örnek 2: geçerli abonelikteki tüm Web hizmeti kaynaklarını edinin--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4d11-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="c4d11-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="c4d11-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="c4d11-113">--------------------------Örnek 3: geçerli abonelikteki ve verilen kaynak grubundaki tüm Web hizmetlerini edinin--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4d11-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="c4d11-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="c4d11-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="c4d11-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4d11-115">PARAMETERS</span></span>

### <span data-ttu-id="c4d11-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4d11-116">-Name</span></span>
<span data-ttu-id="c4d11-117">Ayrıntılarının alındığı Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="c4d11-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="c4d11-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d11-118">-ResourceGroupName</span></span>
<span data-ttu-id="c4d11-119">Web servisinin ayrıntılarının alındığı kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="c4d11-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="c4d11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d11-120">-DefaultProfile</span></span>
<span data-ttu-id="c4d11-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4d11-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4d11-122">-Bölge</span><span class="sxs-lookup"><span data-stu-id="c4d11-122">-Region</span></span>
<span data-ttu-id="c4d11-123">Bölge adı</span><span class="sxs-lookup"><span data-stu-id="c4d11-123">The name of region</span></span>

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

### <span data-ttu-id="c4d11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d11-124">CommonParameters</span></span>
<span data-ttu-id="c4d11-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4d11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d11-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d11-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d11-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4d11-127">INPUTS</span></span>

## <span data-ttu-id="c4d11-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4d11-128">OUTPUTS</span></span>

### <span data-ttu-id="c4d11-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c4d11-129">None</span></span>

## <span data-ttu-id="c4d11-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4d11-130">NOTES</span></span>
<span data-ttu-id="c4d11-131">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="c4d11-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c4d11-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4d11-132">RELATED LINKS</span></span>

