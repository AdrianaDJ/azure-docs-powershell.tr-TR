---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: 4d7365a2a7a8d11fc1032f182409bd462931be3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590452"
---
# <span data-ttu-id="af3ec-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="af3ec-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="af3ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="af3ec-103">Web hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="af3ec-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af3ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af3ec-104">SYNTAX</span></span>

### <span data-ttu-id="af3ec-105">Removebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="af3ec-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af3ec-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="af3ec-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af3ec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af3ec-107">DESCRIPTION</span></span>
<span data-ttu-id="af3ec-108">Kaynak grubu ve adıyla başvurulan bir Azure Machine Learning Web hizmetini siler.</span><span class="sxs-lookup"><span data-stu-id="af3ec-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="af3ec-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af3ec-109">EXAMPLES</span></span>

### <span data-ttu-id="af3ec-110">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="af3ec-110">--------------------------  Example 1  --------------------------</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="af3ec-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af3ec-111">PARAMETERS</span></span>

### <span data-ttu-id="af3ec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3ec-112">-DefaultProfile</span></span>
<span data-ttu-id="af3ec-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="af3ec-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af3ec-114">-Force</span><span class="sxs-lookup"><span data-stu-id="af3ec-114">-Force</span></span>
<span data-ttu-id="af3ec-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="af3ec-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="af3ec-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="af3ec-116">-MlWebService</span></span>
<span data-ttu-id="af3ec-117">Kaldırılacak Web hizmeti.</span><span class="sxs-lookup"><span data-stu-id="af3ec-117">The web service to be removed.</span></span>

```yaml
Type: WebService
Parameter Sets: RemoveByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af3ec-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="af3ec-118">-Name</span></span>
<span data-ttu-id="af3ec-119">Kaldırılacak Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="af3ec-119">The name of the web service to be removed.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af3ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af3ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="af3ec-121">Web hizmetinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="af3ec-121">The resource group of the web service.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af3ec-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="af3ec-122">-Confirm</span></span>
<span data-ttu-id="af3ec-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af3ec-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af3ec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af3ec-124">-WhatIf</span></span>
<span data-ttu-id="af3ec-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af3ec-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af3ec-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af3ec-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af3ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3ec-127">CommonParameters</span></span>
<span data-ttu-id="af3ec-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af3ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3ec-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af3ec-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3ec-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af3ec-130">INPUTS</span></span>

### <span data-ttu-id="af3ec-131">Konumundaki</span><span class="sxs-lookup"><span data-stu-id="af3ec-131">WebService</span></span>
<span data-ttu-id="af3ec-132">' MlWebService ' parametresi ardışık düzenin ' WebService ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="af3ec-132">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="af3ec-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af3ec-133">OUTPUTS</span></span>

### <span data-ttu-id="af3ec-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="af3ec-134">None</span></span>

## <span data-ttu-id="af3ec-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af3ec-135">NOTES</span></span>
<span data-ttu-id="af3ec-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="af3ec-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="af3ec-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af3ec-137">RELATED LINKS</span></span>

