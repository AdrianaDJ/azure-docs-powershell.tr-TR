---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/add-azurermmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b2f881b57639a83227c2f590ffd260b78509a54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594071"
---
# <span data-ttu-id="bcb37-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="bcb37-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="bcb37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcb37-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb37-103">Bölgesel Web hizmeti özellikleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bcb37-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bcb37-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcb37-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcb37-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb37-106">Var olan bir Web hizmeti için Azure makine Learning bölgesel özelliklerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bcb37-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="bcb37-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bcb37-107">EXAMPLES</span></span>

### <span data-ttu-id="bcb37-108">--------------------------Örnek 1: Batı merkezi ABD için yeni bölgesel özellikler--------------------------</span><span class="sxs-lookup"><span data-stu-id="bcb37-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="bcb37-109">Bu örnek komut, "Batı merkezi" bölgesindeki bir Web hizmeti için bölgesel özellik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bcb37-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="bcb37-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bcb37-110">PARAMETERS</span></span>

### <span data-ttu-id="bcb37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb37-111">-DefaultProfile</span></span>
<span data-ttu-id="bcb37-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bcb37-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcb37-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bcb37-113">-Force</span></span>
<span data-ttu-id="bcb37-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="bcb37-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bcb37-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bcb37-115">-Name</span></span>
<span data-ttu-id="bcb37-116">Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="bcb37-116">The name for the web service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb37-117">-Bölge</span><span class="sxs-lookup"><span data-stu-id="bcb37-117">-Region</span></span>
<span data-ttu-id="bcb37-118">Web hizmeti özelliklerinin oluşturulacağı bölge.</span><span class="sxs-lookup"><span data-stu-id="bcb37-118">The region in which to create the web service properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb37-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb37-119">-ResourceGroupName</span></span>
<span data-ttu-id="bcb37-120">Web servisinin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bcb37-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb37-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="bcb37-121">-Confirm</span></span>
<span data-ttu-id="bcb37-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bcb37-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcb37-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb37-123">-WhatIf</span></span>
<span data-ttu-id="bcb37-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bcb37-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb37-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bcb37-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcb37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb37-126">CommonParameters</span></span>
<span data-ttu-id="bcb37-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bcb37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb37-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb37-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb37-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bcb37-129">INPUTS</span></span>

### <span data-ttu-id="bcb37-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bcb37-130">None</span></span>
<span data-ttu-id="bcb37-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bcb37-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bcb37-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bcb37-132">OUTPUTS</span></span>

### <span data-ttu-id="bcb37-133">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="bcb37-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="bcb37-134">Azure Machine Learning Web hizmetinin Özet açıklaması.</span><span class="sxs-lookup"><span data-stu-id="bcb37-134">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="bcb37-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bcb37-135">NOTES</span></span>
<span data-ttu-id="bcb37-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="bcb37-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="bcb37-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bcb37-137">RELATED LINKS</span></span>

