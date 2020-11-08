---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278932"
---
# <span data-ttu-id="5a10c-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="5a10c-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="5a10c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a10c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a10c-103">JSON nesnesini Web hizmeti tanımına aktarır.</span><span class="sxs-lookup"><span data-stu-id="5a10c-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="5a10c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a10c-104">SYNTAX</span></span>

### <span data-ttu-id="5a10c-105">Importfromjsonfile</span><span class="sxs-lookup"><span data-stu-id="5a10c-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a10c-106">Importfromjsonstring.</span><span class="sxs-lookup"><span data-stu-id="5a10c-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a10c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a10c-107">DESCRIPTION</span></span>
<span data-ttu-id="5a10c-108">Import-AzMlWebService cmdlet, doğrudan veya başvurulan bir dosyada belirtilir ve New-AzMlWebService cmdlet 'ine geçirilebilecek bir Web hizmeti tanım nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a10c-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="5a10c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a10c-109">EXAMPLES</span></span>

### <span data-ttu-id="5a10c-110">Örnek 1: dizeden Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="5a10c-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="5a10c-111">Örnek 2: dosya yolundan Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="5a10c-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="5a10c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a10c-112">PARAMETERS</span></span>

### <span data-ttu-id="5a10c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a10c-113">-DefaultProfile</span></span>
<span data-ttu-id="5a10c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5a10c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a10c-115">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="5a10c-115">-InputFile</span></span>
<span data-ttu-id="5a10c-116">İçeri aktarılacak Web hizmeti tanımını içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="5a10c-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="5a10c-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="5a10c-117">-JsonString</span></span>
<span data-ttu-id="5a10c-118">İçeri aktarılacak Web hizmeti tanımını içeren JSON biçimli dize.</span><span class="sxs-lookup"><span data-stu-id="5a10c-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="5a10c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a10c-119">CommonParameters</span></span>
<span data-ttu-id="5a10c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a10c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a10c-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a10c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a10c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a10c-122">INPUTS</span></span>

### <span data-ttu-id="5a10c-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5a10c-123">None</span></span>

## <span data-ttu-id="5a10c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a10c-124">OUTPUTS</span></span>

### <span data-ttu-id="5a10c-125">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="5a10c-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="5a10c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a10c-126">NOTES</span></span>
<span data-ttu-id="5a10c-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5a10c-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5a10c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a10c-128">RELATED LINKS</span></span>
