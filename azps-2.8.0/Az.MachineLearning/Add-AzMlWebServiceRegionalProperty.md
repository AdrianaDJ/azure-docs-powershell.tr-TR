---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 877ef93dbecf3510887a24cb0b5dfe65948658f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751470"
---
# <span data-ttu-id="82b2a-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="82b2a-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="82b2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="82b2a-103">Bölgesel Web hizmeti özellikleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82b2a-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="82b2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82b2a-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82b2a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82b2a-105">DESCRIPTION</span></span>
<span data-ttu-id="82b2a-106">Var olan bir Web hizmeti için Azure makine Learning bölgesel özelliklerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82b2a-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="82b2a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82b2a-107">EXAMPLES</span></span>

### <span data-ttu-id="82b2a-108">Örnek 1: Batı merkezi ABD için yeni bölgesel özellikler ekleme</span><span class="sxs-lookup"><span data-stu-id="82b2a-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="82b2a-109">Bu örnek komut, "Batı merkezi" bölgesindeki bir Web hizmeti için bölgesel özellik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82b2a-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="82b2a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82b2a-110">PARAMETERS</span></span>

### <span data-ttu-id="82b2a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b2a-111">-DefaultProfile</span></span>
<span data-ttu-id="82b2a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="82b2a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82b2a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="82b2a-113">-Force</span></span>
<span data-ttu-id="82b2a-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="82b2a-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="82b2a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="82b2a-115">-Name</span></span>
<span data-ttu-id="82b2a-116">Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="82b2a-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b2a-117">-Bölge</span><span class="sxs-lookup"><span data-stu-id="82b2a-117">-Region</span></span>
<span data-ttu-id="82b2a-118">Web hizmeti özelliklerinin oluşturulacağı bölge.</span><span class="sxs-lookup"><span data-stu-id="82b2a-118">The region in which to create the web service properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b2a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b2a-119">-ResourceGroupName</span></span>
<span data-ttu-id="82b2a-120">Web servisinin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="82b2a-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b2a-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="82b2a-121">-Confirm</span></span>
<span data-ttu-id="82b2a-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="82b2a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82b2a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82b2a-123">-WhatIf</span></span>
<span data-ttu-id="82b2a-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82b2a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82b2a-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="82b2a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82b2a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b2a-126">CommonParameters</span></span>
<span data-ttu-id="82b2a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82b2a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b2a-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82b2a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b2a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82b2a-129">INPUTS</span></span>

### <span data-ttu-id="82b2a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="82b2a-130">System.String</span></span>

## <span data-ttu-id="82b2a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82b2a-131">OUTPUTS</span></span>

### <span data-ttu-id="82b2a-132">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="82b2a-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="82b2a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82b2a-133">NOTES</span></span>
<span data-ttu-id="82b2a-134">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="82b2a-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="82b2a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82b2a-135">RELATED LINKS</span></span>
