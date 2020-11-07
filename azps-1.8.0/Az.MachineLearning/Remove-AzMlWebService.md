---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 2ade770ea51f3b9cb83ff04fc5edf604cab5bb71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915851"
---
# <span data-ttu-id="8dd92-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="8dd92-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="8dd92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dd92-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd92-103">Web hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="8dd92-103">Deletes a web service.</span></span>

## <span data-ttu-id="8dd92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8dd92-104">SYNTAX</span></span>

### <span data-ttu-id="8dd92-105">Removebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="8dd92-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dd92-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="8dd92-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd92-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8dd92-107">DESCRIPTION</span></span>
<span data-ttu-id="8dd92-108">Kaynak grubu ve adıyla başvurulan bir Azure Machine Learning Web hizmetini siler.</span><span class="sxs-lookup"><span data-stu-id="8dd92-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="8dd92-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8dd92-109">EXAMPLES</span></span>

### <span data-ttu-id="8dd92-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8dd92-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="8dd92-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8dd92-111">PARAMETERS</span></span>

### <span data-ttu-id="8dd92-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd92-112">-DefaultProfile</span></span>
<span data-ttu-id="8dd92-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8dd92-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dd92-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8dd92-114">-Force</span></span>
<span data-ttu-id="8dd92-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="8dd92-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8dd92-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="8dd92-116">-MlWebService</span></span>
<span data-ttu-id="8dd92-117">Kaldırılacak Web hizmeti.</span><span class="sxs-lookup"><span data-stu-id="8dd92-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="8dd92-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="8dd92-118">-Name</span></span>
<span data-ttu-id="8dd92-119">Kaldırılacak Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="8dd92-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="8dd92-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd92-120">-ResourceGroupName</span></span>
<span data-ttu-id="8dd92-121">Web hizmetinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8dd92-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="8dd92-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="8dd92-122">-Confirm</span></span>
<span data-ttu-id="8dd92-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8dd92-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd92-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd92-124">-WhatIf</span></span>
<span data-ttu-id="8dd92-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dd92-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dd92-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8dd92-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd92-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd92-127">CommonParameters</span></span>
<span data-ttu-id="8dd92-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8dd92-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd92-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd92-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd92-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8dd92-130">INPUTS</span></span>

### <span data-ttu-id="8dd92-131">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="8dd92-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="8dd92-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8dd92-132">OUTPUTS</span></span>

### <span data-ttu-id="8dd92-133">System. void</span><span class="sxs-lookup"><span data-stu-id="8dd92-133">System.Void</span></span>

## <span data-ttu-id="8dd92-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8dd92-134">NOTES</span></span>
<span data-ttu-id="8dd92-135">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="8dd92-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8dd92-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8dd92-136">RELATED LINKS</span></span>
