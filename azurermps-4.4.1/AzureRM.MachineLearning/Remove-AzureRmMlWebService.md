---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592202"
---
# <span data-ttu-id="40469-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="40469-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="40469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40469-102">SYNOPSIS</span></span>
<span data-ttu-id="40469-103">Web hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="40469-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40469-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40469-104">SYNTAX</span></span>

### <span data-ttu-id="40469-105">Ad ve kaynak grubuna göre Azure ML Web hizmeti kaynağı 'nı kaldırın.</span><span class="sxs-lookup"><span data-stu-id="40469-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40469-106">Nesne olarak belirtilen bir Azure ML Web hizmetini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="40469-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40469-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="40469-107">DESCRIPTION</span></span>
<span data-ttu-id="40469-108">Kaynak grubu ve adıyla başvurulan bir Azure Machine Learning Web hizmetini siler.</span><span class="sxs-lookup"><span data-stu-id="40469-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="40469-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40469-109">EXAMPLES</span></span>

### <span data-ttu-id="40469-110">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="40469-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="40469-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="40469-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="40469-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40469-112">PARAMETERS</span></span>

### <span data-ttu-id="40469-113">-Force</span><span class="sxs-lookup"><span data-stu-id="40469-113">-Force</span></span>
<span data-ttu-id="40469-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="40469-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="40469-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="40469-115">-MlWebService</span></span>
<span data-ttu-id="40469-116">Kaldırılacak Web hizmeti.</span><span class="sxs-lookup"><span data-stu-id="40469-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40469-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="40469-117">-Name</span></span>
<span data-ttu-id="40469-118">Kaldırılacak Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="40469-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40469-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40469-119">-ResourceGroupName</span></span>
<span data-ttu-id="40469-120">Web hizmetinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="40469-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40469-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="40469-121">-Confirm</span></span>
<span data-ttu-id="40469-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40469-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40469-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40469-123">-WhatIf</span></span>
<span data-ttu-id="40469-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40469-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40469-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40469-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40469-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40469-126">-DefaultProfile</span></span>
<span data-ttu-id="40469-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40469-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40469-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40469-128">CommonParameters</span></span>
<span data-ttu-id="40469-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40469-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40469-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40469-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40469-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40469-131">INPUTS</span></span>

### <span data-ttu-id="40469-132">Konumundaki</span><span class="sxs-lookup"><span data-stu-id="40469-132">WebService</span></span>
<span data-ttu-id="40469-133">' MlWebService ' parametresi ardışık düzenin ' WebService ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="40469-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="40469-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40469-134">OUTPUTS</span></span>

### <span data-ttu-id="40469-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="40469-135">None</span></span>

## <span data-ttu-id="40469-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40469-136">NOTES</span></span>
<span data-ttu-id="40469-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="40469-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="40469-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40469-138">RELATED LINKS</span></span>

