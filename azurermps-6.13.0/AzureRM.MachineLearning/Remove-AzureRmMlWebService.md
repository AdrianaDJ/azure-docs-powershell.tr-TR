---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: c1d6ae6c1396e23398bc1b52f4f32458999072a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590882"
---
# <span data-ttu-id="4d861-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="4d861-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="4d861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d861-102">SYNOPSIS</span></span>
<span data-ttu-id="4d861-103">Web hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="4d861-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d861-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d861-104">SYNTAX</span></span>

### <span data-ttu-id="4d861-105">Removebynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="4d861-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d861-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4d861-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d861-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d861-107">DESCRIPTION</span></span>
<span data-ttu-id="4d861-108">Kaynak grubu ve adıyla başvurulan bir Azure Machine Learning Web hizmetini siler.</span><span class="sxs-lookup"><span data-stu-id="4d861-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="4d861-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d861-109">EXAMPLES</span></span>

### <span data-ttu-id="4d861-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4d861-110">Example 1</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="4d861-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d861-111">PARAMETERS</span></span>

### <span data-ttu-id="4d861-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d861-112">-DefaultProfile</span></span>
<span data-ttu-id="4d861-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4d861-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d861-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4d861-114">-Force</span></span>
<span data-ttu-id="4d861-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="4d861-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4d861-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="4d861-116">-MlWebService</span></span>
<span data-ttu-id="4d861-117">Kaldırılacak Web hizmeti.</span><span class="sxs-lookup"><span data-stu-id="4d861-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="4d861-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d861-118">-Name</span></span>
<span data-ttu-id="4d861-119">Kaldırılacak Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="4d861-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="4d861-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d861-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d861-121">Web hizmetinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="4d861-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="4d861-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d861-122">-Confirm</span></span>
<span data-ttu-id="4d861-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d861-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d861-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d861-124">-WhatIf</span></span>
<span data-ttu-id="4d861-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d861-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d861-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d861-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d861-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d861-127">CommonParameters</span></span>
<span data-ttu-id="4d861-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d861-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d861-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d861-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d861-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d861-130">INPUTS</span></span>

### <span data-ttu-id="4d861-131">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="4d861-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="4d861-132">Parametreler: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d861-132">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="4d861-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d861-133">OUTPUTS</span></span>

### <span data-ttu-id="4d861-134">System. void</span><span class="sxs-lookup"><span data-stu-id="4d861-134">System.Void</span></span>

## <span data-ttu-id="4d861-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d861-135">NOTES</span></span>
<span data-ttu-id="4d861-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="4d861-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4d861-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d861-137">RELATED LINKS</span></span>