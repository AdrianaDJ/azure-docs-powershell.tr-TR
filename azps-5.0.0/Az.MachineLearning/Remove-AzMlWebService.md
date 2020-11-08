---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278923"
---
# <span data-ttu-id="fd938-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="fd938-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="fd938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd938-102">SYNOPSIS</span></span>
<span data-ttu-id="fd938-103">Web hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="fd938-103">Deletes a web service.</span></span>

## <span data-ttu-id="fd938-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd938-104">SYNTAX</span></span>

### <span data-ttu-id="fd938-105">Removebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="fd938-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd938-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="fd938-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd938-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd938-107">DESCRIPTION</span></span>
<span data-ttu-id="fd938-108">Kaynak grubu ve adıyla başvurulan bir Azure Machine Learning Web hizmetini siler.</span><span class="sxs-lookup"><span data-stu-id="fd938-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="fd938-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd938-109">EXAMPLES</span></span>

### <span data-ttu-id="fd938-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fd938-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="fd938-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd938-111">PARAMETERS</span></span>

### <span data-ttu-id="fd938-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd938-112">-DefaultProfile</span></span>
<span data-ttu-id="fd938-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fd938-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd938-114">-Force</span><span class="sxs-lookup"><span data-stu-id="fd938-114">-Force</span></span>
<span data-ttu-id="fd938-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="fd938-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fd938-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="fd938-116">-MlWebService</span></span>
<span data-ttu-id="fd938-117">Kaldırılacak Web hizmeti.</span><span class="sxs-lookup"><span data-stu-id="fd938-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd938-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd938-118">-Name</span></span>
<span data-ttu-id="fd938-119">Kaldırılacak Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="fd938-119">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd938-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd938-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd938-121">Web hizmetinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fd938-121">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd938-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd938-122">-Confirm</span></span>
<span data-ttu-id="fd938-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd938-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd938-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd938-124">-WhatIf</span></span>
<span data-ttu-id="fd938-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd938-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd938-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd938-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd938-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd938-127">CommonParameters</span></span>
<span data-ttu-id="fd938-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd938-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd938-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd938-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd938-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd938-130">INPUTS</span></span>

### <span data-ttu-id="fd938-131">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="fd938-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="fd938-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd938-132">OUTPUTS</span></span>

### <span data-ttu-id="fd938-133">System. void</span><span class="sxs-lookup"><span data-stu-id="fd938-133">System.Void</span></span>

## <span data-ttu-id="fd938-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd938-134">NOTES</span></span>
<span data-ttu-id="fd938-135">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="fd938-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fd938-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd938-136">RELATED LINKS</span></span>
