---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: d85767623d88c9fd7d0a00ea98e575953132d3f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764820"
---
# <span data-ttu-id="8e0f4-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="8e0f4-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="8e0f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0f4-103">JSON nesnesini Web hizmeti tanımına aktarır.</span><span class="sxs-lookup"><span data-stu-id="8e0f4-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e0f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e0f4-104">SYNTAX</span></span>

### <span data-ttu-id="8e0f4-105">JSON dosyasından içeri aktarma.</span><span class="sxs-lookup"><span data-stu-id="8e0f4-105">Import from JSON file.</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e0f4-106">JSON dizesinden içeri aktarma.</span><span class="sxs-lookup"><span data-stu-id="8e0f4-106">Import from JSON string.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e0f4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e0f4-107">DESCRIPTION</span></span>
<span data-ttu-id="8e0f4-108">Import-AzureRmMlWebService cmdlet, doğrudan veya başvurulan bir dosyada belirtilir ve New-AzureRmMlWebService cmdlet 'ine geçirilebilecek bir Web hizmeti tanım nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e0f4-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="8e0f4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e0f4-109">EXAMPLES</span></span>

### <span data-ttu-id="8e0f4-110">--------------------------: Dizeden Içeri aktarma--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e0f4-110">--------------------------  Example 1: Import from string  --------------------------</span></span>
<span data-ttu-id="8e0f4-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="8e0f4-111">@{paragraph=PS C:\\\>}</span></span>





```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="8e0f4-112">--------------------------Örnek 2: dosya yolundan Içeri aktarma--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e0f4-112">--------------------------  Example 2: Import from file path  --------------------------</span></span>
<span data-ttu-id="8e0f4-113">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="8e0f4-113">@{paragraph=PS C:\\\>}</span></span>





```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="8e0f4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e0f4-114">PARAMETERS</span></span>

### <span data-ttu-id="8e0f4-115">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="8e0f4-115">-InputFile</span></span>
<span data-ttu-id="8e0f4-116">İçeri aktarılacak Web hizmeti tanımını içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="8e0f4-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: Import from JSON file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0f4-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="8e0f4-117">-JsonString</span></span>
<span data-ttu-id="8e0f4-118">İçeri aktarılacak Web hizmeti tanımını içeren JSON biçimli dize.</span><span class="sxs-lookup"><span data-stu-id="8e0f4-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: Import from JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0f4-119">-DefaultProfile</span></span>
<span data-ttu-id="8e0f4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e0f4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e0f4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0f4-121">CommonParameters</span></span>
<span data-ttu-id="8e0f4-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e0f4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0f4-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e0f4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0f4-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e0f4-124">INPUTS</span></span>

## <span data-ttu-id="8e0f4-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e0f4-125">OUTPUTS</span></span>

### <span data-ttu-id="8e0f4-126">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="8e0f4-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="8e0f4-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e0f4-127">NOTES</span></span>
<span data-ttu-id="8e0f4-128">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="8e0f4-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8e0f4-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e0f4-129">RELATED LINKS</span></span>

