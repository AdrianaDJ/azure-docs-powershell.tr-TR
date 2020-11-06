---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: fd07ab55fad93fdf48df52e15db846630ba6c1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594070"
---
# <span data-ttu-id="d842c-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="d842c-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="d842c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d842c-102">SYNOPSIS</span></span>
<span data-ttu-id="d842c-103">Web hizmeti tanım nesnesini JSON biçimli dize olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="d842c-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d842c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d842c-104">SYNTAX</span></span>

### <span data-ttu-id="d842c-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="d842c-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d842c-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="d842c-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d842c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d842c-107">DESCRIPTION</span></span>
<span data-ttu-id="d842c-108">Belirtilen Web servonun tanım nesnesini, JSON ile biçimlendirilmiş dize olarak dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="d842c-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="d842c-109">Dizeyi hemen döndürebilir veya dosyaya kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d842c-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="d842c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d842c-110">EXAMPLES</span></span>

### <span data-ttu-id="d842c-111">--------------------------Örnek 1: dize olarak dışarı aktar--------------------------</span><span class="sxs-lookup"><span data-stu-id="d842c-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="d842c-112">--------------------------Örnek 2: dosyaya aktar--------------------------</span><span class="sxs-lookup"><span data-stu-id="d842c-112">--------------------------  Example 2: Export to file  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="d842c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d842c-113">PARAMETERS</span></span>

### <span data-ttu-id="d842c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d842c-114">-DefaultProfile</span></span>
<span data-ttu-id="d842c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d842c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d842c-116">-Force</span></span>
<span data-ttu-id="d842c-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="d842c-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-118">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="d842c-118">-OutputFile</span></span>
<span data-ttu-id="d842c-119">Dışarı aktarılan tanım için dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="d842c-119">The file path for exported definition.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="d842c-120">-ToJsonString</span></span>
<span data-ttu-id="d842c-121">Tanımın JSON dizesi olarak dışarı aktarılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d842c-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToJSON
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="d842c-122">-WebService</span></span>
<span data-ttu-id="d842c-123">Dışarı aktarılacak Web hizmeti tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d842c-123">The web service definition object to be exported.</span></span>

```yaml
Type: WebService
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="d842c-124">-Confirm</span></span>
<span data-ttu-id="d842c-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d842c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d842c-126">-WhatIf</span></span>
<span data-ttu-id="d842c-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d842c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d842c-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d842c-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d842c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d842c-129">CommonParameters</span></span>
<span data-ttu-id="d842c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d842c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d842c-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d842c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d842c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d842c-132">INPUTS</span></span>

### <span data-ttu-id="d842c-133">Konumundaki</span><span class="sxs-lookup"><span data-stu-id="d842c-133">WebService</span></span>
<span data-ttu-id="d842c-134">' WebService ' parametresi ardışık düzenin ' WebService ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d842c-134">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="d842c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d842c-135">OUTPUTS</span></span>

### <span data-ttu-id="d842c-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d842c-136">None</span></span>

## <span data-ttu-id="d842c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d842c-137">NOTES</span></span>
<span data-ttu-id="d842c-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d842c-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d842c-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d842c-139">RELATED LINKS</span></span>

