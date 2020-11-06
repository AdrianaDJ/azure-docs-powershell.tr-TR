---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: b54e7cf5af7eadd0ea56687a336175650b55daa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590200"
---
# <span data-ttu-id="27366-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="27366-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="27366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27366-102">SYNOPSIS</span></span>
<span data-ttu-id="27366-103">JSON nesnesini Web hizmeti tanımına aktarır.</span><span class="sxs-lookup"><span data-stu-id="27366-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27366-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27366-104">SYNTAX</span></span>

### <span data-ttu-id="27366-105">Importfromjsonfile</span><span class="sxs-lookup"><span data-stu-id="27366-105">ImportFromJSONFile</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27366-106">Importfromjsonstring.</span><span class="sxs-lookup"><span data-stu-id="27366-106">ImportFromJSONString.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27366-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="27366-107">DESCRIPTION</span></span>
<span data-ttu-id="27366-108">Import-AzureRmMlWebService cmdlet, doğrudan veya başvurulan bir dosyada belirtilir ve New-AzureRmMlWebService cmdlet 'ine geçirilebilecek bir Web hizmeti tanım nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27366-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="27366-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27366-109">EXAMPLES</span></span>

### <span data-ttu-id="27366-110">Örnek 1: dizeden Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="27366-110">Example 1: Import from string</span></span>
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="27366-111">Örnek 2: dosya yolundan Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="27366-111">Example 2: Import from file path</span></span>
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="27366-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27366-112">PARAMETERS</span></span>

### <span data-ttu-id="27366-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27366-113">-DefaultProfile</span></span>
<span data-ttu-id="27366-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="27366-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27366-115">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="27366-115">-InputFile</span></span>
<span data-ttu-id="27366-116">İçeri aktarılacak Web hizmeti tanımını içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="27366-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27366-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="27366-117">-JsonString</span></span>
<span data-ttu-id="27366-118">İçeri aktarılacak Web hizmeti tanımını içeren JSON biçimli dize.</span><span class="sxs-lookup"><span data-stu-id="27366-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27366-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27366-119">CommonParameters</span></span>
<span data-ttu-id="27366-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27366-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27366-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27366-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27366-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27366-122">INPUTS</span></span>

### <span data-ttu-id="27366-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="27366-123">None</span></span>

## <span data-ttu-id="27366-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27366-124">OUTPUTS</span></span>

### <span data-ttu-id="27366-125">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="27366-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="27366-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27366-126">NOTES</span></span>
<span data-ttu-id="27366-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="27366-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="27366-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27366-128">RELATED LINKS</span></span>
