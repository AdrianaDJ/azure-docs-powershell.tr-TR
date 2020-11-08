---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280117"
---
# <span data-ttu-id="080de-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="080de-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="080de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="080de-102">SYNOPSIS</span></span>
<span data-ttu-id="080de-103">Web hizmeti tanım nesnesini JSON biçimli dize olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="080de-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="080de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="080de-104">SYNTAX</span></span>

### <span data-ttu-id="080de-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="080de-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="080de-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="080de-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="080de-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="080de-107">DESCRIPTION</span></span>
<span data-ttu-id="080de-108">Belirtilen Web hizmeti için tanım nesnesini JSON biçimli dize olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="080de-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="080de-109">Dizeyi hemen döndürebilir veya dosyaya kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="080de-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="080de-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="080de-110">EXAMPLES</span></span>

### <span data-ttu-id="080de-111">Örnek 1: dize olarak dışarı aktar</span><span class="sxs-lookup"><span data-stu-id="080de-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="080de-112">Örnek 2: dosyaya aktar</span><span class="sxs-lookup"><span data-stu-id="080de-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="080de-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="080de-113">PARAMETERS</span></span>

### <span data-ttu-id="080de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="080de-114">-DefaultProfile</span></span>
<span data-ttu-id="080de-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="080de-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="080de-116">-Force</span><span class="sxs-lookup"><span data-stu-id="080de-116">-Force</span></span>
<span data-ttu-id="080de-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="080de-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="080de-118">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="080de-118">-OutputFile</span></span>
<span data-ttu-id="080de-119">Dışarı aktarılan tanım için dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="080de-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="080de-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="080de-120">-ToJsonString</span></span>
<span data-ttu-id="080de-121">Tanımın JSON dizesi olarak dışarı aktarılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="080de-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="080de-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="080de-122">-WebService</span></span>
<span data-ttu-id="080de-123">Dışarı aktarılacak Web hizmeti tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="080de-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="080de-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="080de-124">-Confirm</span></span>
<span data-ttu-id="080de-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="080de-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="080de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="080de-126">-WhatIf</span></span>
<span data-ttu-id="080de-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="080de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="080de-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="080de-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="080de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="080de-129">CommonParameters</span></span>
<span data-ttu-id="080de-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="080de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="080de-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="080de-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="080de-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="080de-132">INPUTS</span></span>

### <span data-ttu-id="080de-133">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="080de-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="080de-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="080de-134">OUTPUTS</span></span>

### <span data-ttu-id="080de-135">System. String</span><span class="sxs-lookup"><span data-stu-id="080de-135">System.String</span></span>

## <span data-ttu-id="080de-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="080de-136">NOTES</span></span>
<span data-ttu-id="080de-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="080de-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="080de-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="080de-138">RELATED LINKS</span></span>
