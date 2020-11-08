---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098267"
---
# <span data-ttu-id="59d0d-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="59d0d-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="59d0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="59d0d-103">Web hizmeti tanım nesnesini JSON biçimli dize olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="59d0d-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="59d0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59d0d-104">SYNTAX</span></span>

### <span data-ttu-id="59d0d-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="59d0d-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d0d-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="59d0d-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d0d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="59d0d-107">DESCRIPTION</span></span>
<span data-ttu-id="59d0d-108">Belirtilen Web hizmeti için tanım nesnesini JSON biçimli dize olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="59d0d-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="59d0d-109">Dizeyi hemen döndürebilir veya dosyaya kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59d0d-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="59d0d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59d0d-110">EXAMPLES</span></span>

### <span data-ttu-id="59d0d-111">Örnek 1: dize olarak dışarı aktar</span><span class="sxs-lookup"><span data-stu-id="59d0d-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="59d0d-112">Örnek 2: dosyaya aktar</span><span class="sxs-lookup"><span data-stu-id="59d0d-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="59d0d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59d0d-113">PARAMETERS</span></span>

### <span data-ttu-id="59d0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d0d-114">-DefaultProfile</span></span>
<span data-ttu-id="59d0d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="59d0d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59d0d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="59d0d-116">-Force</span></span>
<span data-ttu-id="59d0d-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="59d0d-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d0d-118">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="59d0d-118">-OutputFile</span></span>
<span data-ttu-id="59d0d-119">Dışarı aktarılan tanım için dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="59d0d-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d0d-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="59d0d-120">-ToJsonString</span></span>
<span data-ttu-id="59d0d-121">Tanımın JSON dizesi olarak dışarı aktarılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59d0d-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d0d-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="59d0d-122">-WebService</span></span>
<span data-ttu-id="59d0d-123">Dışarı aktarılacak Web hizmeti tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="59d0d-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59d0d-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="59d0d-124">-Confirm</span></span>
<span data-ttu-id="59d0d-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59d0d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d0d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d0d-126">-WhatIf</span></span>
<span data-ttu-id="59d0d-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59d0d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59d0d-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59d0d-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d0d-129">CommonParameters</span></span>
<span data-ttu-id="59d0d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59d0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d0d-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d0d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d0d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59d0d-132">INPUTS</span></span>

### <span data-ttu-id="59d0d-133">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="59d0d-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="59d0d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59d0d-134">OUTPUTS</span></span>

### <span data-ttu-id="59d0d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="59d0d-135">System.String</span></span>

## <span data-ttu-id="59d0d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59d0d-136">NOTES</span></span>
<span data-ttu-id="59d0d-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="59d0d-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="59d0d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59d0d-138">RELATED LINKS</span></span>